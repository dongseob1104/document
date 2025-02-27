MariaDB DUMP 명령

1. 백업

mysqldump -u [아이디] -p '[패스워드]' --all-databases > [백업파일명].sql // 데이터베이스 전체 백업

example: mysqldump -u IdContent -p 'PasswordContent' --all-databases > Backup_File_Content.sql

// 값 없이 복구 // mysqldump -u [아이디] -p '[패스워드]' --all-databases --no-data > [백업파일명].sql

mysqldump -u [아이디] -p '[패스워드]' [스키마 이름] > [백업파일명].sql // 특정 스키마의 백업

example: mysqldump -u IdContent -p 'PasswordContent' schemaContent > Backup_File_Content.sql

만약 윈도에서 도커 db에 백업 또는 복구 진행하려면 sql 파일을 복사해서 리눅스 환경에 넣고 진행해야 함
-> docker cp [컨테이너 이름]:[경로/파일이름.sql] [윈도 복제할 경로 지정]
-> example) docker cp mariadb-10.5.5:/home/test.sql C:/

복제하는 도중 권한 문제가 발생할 수 있음
파워쉘을 관리자 모드로 실행후 명령 날릴 것

-> docker exec -i mariadb mysqldump -u root -p [스키마 이름] > [사용할 이름].sql
-> example) mysqldump -u root -p c_plat_iot > test.sql

/////////
원격
////////
mysqldump -h '[호스트]' -u [아이디] -p '[패스워드]' --port [포트번호] --all-databases > [백업파일명].sql // 원격으로 데이터베이스 전체 백업

example: mysqldump -h '[호스트]' -u IdContent -p 'PasswordContent' --port PortContent --all-databases > Backup_File_Content.sql
///////////////

2. 복구

mysql -u [아이디] -p '[패스워드]' < [백업파일명].sql // 데이터베이스 전체 복구

example: mysql -u IdContent -p 'PasswordContent' < Backup_File_Content.sql

mysql -u [아이디] -p [패스워드] [스키마 이름] < [백업파일명].sql // 특정 스키마의 복구

example: mysql -u IdContent -p 'PasswordContent' schemaContent < Backup_File_Content.sql

만약 윈도에서 도커 db에 백업 또는 복구 진행하려면 sql 파일을 복사해서 리눅스 환경에 넣고 진행해야 함
-> docker cp [파일 위치].sql [이미지 이름]:[경로/파일이름.sql]   mariadb:/backup/backup.sql
-> example) docker cp C:\Users\Desktop\.sql mariadb-10.5.5:home\test.sql

-> docker exec -i mariadb mysql -u root -p[비밀번호] [스키마 이름] < [파일 위치].sql
-> example) mysql -u root -p'root123!@#' c_plat_iot < ./test.sql
// 주의사항 -p부분 붙여야함 // -p'root'
// 보안상으로는 [비밀번호] 빼고 진행할 수 있음

/////////
원격
////////
mysql -h '[호스트]' -u [아이디] -p [패스워드] --port [포트번호] < [백업파일명].sql

example: mysql -h '172.18.61.20' -u root -p 'root123!@#' --port PortContent < C:/Users/Desktop/local.sql
///////////////

// 참고내용 인텔리제이에서 복구 작업 요청한 로그 내용
"C:/Program Files/MariaDB 11.3/bin/mysql.exe" --user=root --host=192.162.61.20 --port=2520 < C:/Users/Desktop/local.sql

////
버전이 높으면 달라질수 있기에 참고 내용
////

mariadb-dump db_name > backup-file.sql

mariadb db_name < backup-file.sql

mariadb -e "source /path-to-backup/backup-file.sql" db_name

mariadb-dump --opt db_name | mariadb --host=remote_host -C db_name

mariadb-dump --databases db_name1 [db_name2 ...] > my_databases.sql

mariadb-dump --all-databases > all_databases.sql

mariadb-dump --all-databases --single-transaction all_databases.sql

mariadb-dump --all-databases --master-data=2 > all_databases.sql

mariadb-dump --all-databases --flush-logs --master-data=2 > all_databases.sql

@Configuration
public class WebConfig implements WebMvcConfigurer {

    @Override
    public void addArgumentResolvers(List<HandlerMethodArgumentResolver> resolvers) {
        resolvers.add(new MemberSearchParamHandlerMethodArgumentResolver());
        resolvers.add(getPageableResolver());
    }

    private PageableHandlerMethodArgumentResolver getPageableResolver() {
        PageableHandlerMethodArgumentResolver resolver = new PageableHandlerMethodArgumentResolver();
        resolver.setOneIndexedParameters(true);
        return resolver;
    }
}

PageableHandlerMethodArgumentResolver

AOP - 관점 지향 프로그래밍을 지원하는 기술

@Aspect -  공통적인 기능들을 모듈화 한것을 의미
관점 지향 프로그래밍(Aspect-Oriented Programming, AOP)
여러 개의 클래스에서 반복해서 사용하는 코드가 있다면 해당 코드를 모듈화 하여 공통 관심사로 분리

# 영속성 (Persistent)

- JPA가 관리하는 상태
- persist(), save() 사용

# 준영속 (Detached)

- 한 번 영속되었다가 JPA가 더 이상 관리하지 않는 상태
- detach(), clear(), close()

# 비영속 (Transient)

- JPA 관리하지 않는 상태
- new 인스턴스

고아객체 (Orphan Removal) - JPA에서 관계가 끊어진 엔티티를 자동으로 삭제해주는 기능 (@조인(orphanRemoval = true))

persist - 추가

# 자동 변경 감지 (Dirty Checking)

- 자동 DB 반영
- 변경감지 사용 소수의 컬럼만 update

merge - 모든 컬럼 내용을 덮어씀 update

벌크 업데이트 - 직접 JPQL 실행
변경 감지 X, JPA의 1차 캐시(영속성 컨텍스트)도 무시됨
컨텍스트 맞추기 위해 벌크가 끝나면
entityManager.clear(); 호출해 1차 캐시 초기화

@Modifying
@Query("UPDATE Product p SET p.price = p.price + 1000 WHERE p.stockQuantity > 0")
int updatePrice();

벌크 INSERT (saveAll()) JDBC Batch 최적화

# OSIV (Open Session In View) / 하이버네이트 - 영속성 컨텍스트를 뷰까지 열어둠

# OEIV (Open EntityManager In View) / JPA - 영속성 컨텍스트를 뷰까지 열어둠

- 영속성 컨텍스트가 트랜잭션 범위가 아닌, HTTP 요청이 끝날 때까지 유지하는 전략

spring:
  jpa:
    open-in-view: true

레핑 (Wrapping) - 어떤 객체나 기능을 감싸서 추가적인 기능을 제공하거나 구조를 변경하는 기법
언래핑 (Unwrapping)

# 비지니스(서비스) 계층

- 핵심 로직 수행
- Service, Facade
- 데이터 검증, 트랜잭션 관리

# 프레젠테이션 계층

- 사용자가 시스템과 상호작용하는 UI(User Interface) 및 컨트롤러 역할을 담당하는 계층
- 사용자 요청/응답 처리
- Controller, View
- JSON, HTML, XML 응답

# 퍼시스턴스(데이터) 계층

- Repository, DAO, EntityManager
- DB 접근

# FACADE 계층

- 여러 개의 서비스, 비즈니스 로직을 하나의 단순한 인터페이스로 감싸서 제공하는 디자인 패턴
- 복잡한 비즈니스 로직을 캡슐화해 코드 가독성 향상

컴포지트 패턴 - 클라이언트가 개별 객체와 객체 그룹을 동일하게 처리할 수 있도록 해주는 패턴

도메인 클래스 컨버터 - @EnableSptirngDataWebSupport

파라미터 바인드
JPQL ?1
네이티브 ?0

@PersistenceContext / EntityManager - 컨테이너가 관리하는 엔티티 매니저 주입 어노테이션

@PersistenceUnit / EntityManagerFactroy - 엔티티 매니저 팩토리 주입 어노테이션
