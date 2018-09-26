# utl-delete-the-last-record-in-a-sas-table
Delete the last record in a sas table. 

    Delete the last record in a sas table;

    github
    https://tinyurl.com/y9yydvaa
    https://github.com/rogerjdeangelis/utl-delete-the-last-record-in-a-sas-table

    SAS Forum
    https://communities.sas.com/t5/SAS-Programming/Delete-last-row-datastep/m-p/498904

    Solution by data_null_
    data _null_,
    datanull@gmail.com


    INPUT
    =====

     WORK.CLASS total obs=18

     Obs    NAME       SEX    AGE    HEIGHT    WEIGHT

       1    Alfred      M      14     69.0      112.5
       2    Alice       F      13     56.5       84.0
       3    Barbara     F      13     65.3       98.0
      ...
      17    Ronald      M      15     67.0      133.0
      18    Thomas      M      11     57.5       85.0
      19    William     M      15     66.5      112.0  ** remove this observation;


    PROCESS
    =======

    data class;
      point=nobs;
      modify class nobs=nobs point=point;
      remove;
      stop;
    run;


    *                _               _       _
     _ __ ___   __ _| | _____     __| | __ _| |_ __ _
    | '_ ` _ \ / _` | |/ / _ \   / _` |/ _` | __/ _` |
    | | | | | | (_| |   <  __/  | (_| | (_| | || (_| |
    |_| |_| |_|\__,_|_|\_\___|   \__,_|\__,_|\__\__,_|

    ;

    data class;
      set sashelp.class;
    run;quit;
