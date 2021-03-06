<h2>Using SQL Plan Management to Control SQL Execution Plans</h2>

Based on <a href="https://blogs.oracle.com/optimizer/using-sql-plan-management-to-control-sql-execution-plans">this blog article.</a>

The example.sql script demonstrates how to control SQL execution plans using SQL plan management. 

The example2.sql calls "proc2.sql": a nice solution that adds a NEW SQL plan baselines and loads all other plans disabled.

Scripts create utility procedures called "set_my_plan" and "add_my_plan" (see proc.sql and proc2.sql) that allows you to take a SQL execution plan from a test query and apply it to an application query.

Example output is shown in example.lst. 

Note that example.sql example2.sql scripts will create a new user called SPM_TESTU.

Scripts tested in Oracle Database 11g Release 2 and Oracle Database 12c Release 2. The only caveat is that in Oracle Database 11g DBMS_XPLAN sometimes returns ORA-01403, but the example still works.


DISCLAIMER:
   <br/>-- These scripts are provided for educational purposes only.
   <br/>-- They are NOT supported by Oracle World Wide Technical Support.
   <br/>-- The scripts have been tested and they appear to work as intended.
   <br/>-- You should always run scripts on a test instance.

