# XML Query

<!-- index start -->

- [Quick Start](/XML_Query)
- [테이블 생성하기](/XML_Query/01_create_schema/)
- [테이블 변경하기](/XML_Query/02_alter_schema/)
- [XML 쿼리 기본](/XML_Query/03_xml_query/)
- [SELECT 쿼리 - 기본](/XML_Query/04_select_query_basic/)
- [SELECT 쿼리 - GROUP BY절](/XML_Query/05_select_query_with_groupby/)
- [SELECT 쿼리 - WHERE절](/XML_Query/06_select_query_with_where/)
- [SELECT 쿼리 - ORDER BY절](/XML_Query/07_select_query_with_navigation/)
- [SELECT 쿼리 - JOIN절](/XML_Query/08_select_query_with_join/)
- [SELECT 쿼리 - 서브쿼리](/XML_Query/09_select_query_with_subquery/)
- [INSERT 쿼리](/XML_Query/10_insert_query/)
- [UPDATE 쿼리](/XML_Query/11_update_query/)
- [DELETE 쿼리](/XML_Query/12_delete_query/)
- [XML 쿼리 실행하기](/XML_Query/13_execute_query/)

<!-- index end -->

## UPDATE 쿼리

```
<query id="updateMember" action="update">
    <tables>
        <table name="member" />
    </tables>
    <columns>
        <column name="password" var="password" notnull="notnull" />
        <column name="user_name" var="user_name" notnull="notnull" minlength="2" maxlength="40" />
    </columns>
    <conditions>
        <condition operation="equal" column="member_srl" var="member_srl" notnull="notnull" filter="number" />
    </conditions>
</query>
```
```
UPDATE xe_member AS member SET password = :password, user_name = :user_name WHERE member_srl = :member_srl;
```

UPDATE 쿼리는 `query` 요소의 `action` 속성을 'update'로 지정합니다.

