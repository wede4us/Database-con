# Database-con
#Microsoft SQL Server

ODBC DSN
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
              "Dsn=DsnName;" + 
              "Uid=UserName;" + 
              "Pwd=Secret;"; 
conn.Open();


ODBC -- Standard Connection
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
              "Driver={SQL Server};" + 
              "Server=DataBaseNamex;" + 
              "DataBase=DataBaseName;" + 
              "Uid=UserName;" + 
              "Pwd=Secret;"; 
conn.Open();


ODBC -- Trusted Connection
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
              "Driver={SQL Server};" + 
              "Server=ServerName;" + 
              "DataBase=DataBaseName;" + 
              "Uid=;" + 
              "Pwd=;"; 
conn.Open();
// or
var conn = new OdbcConnection();
conn.ConnectionString = 
              "Driver={SQL Server};" + 
              "Server=ServerName;" + 
              "DataBase=DataBaseName;" + 
              "Trusted_Connection=Yes;"; 
conn.Open();


OleDb -- Standard Connection
using System.Data.OleDb;
var conn = new OleDbConnection();
conn.ConnectionString = 
              "Driver=SQLOLEDB;" + 
              "Data Source=ServerName;" + 
              "Initial Catalog=DataBaseName;" + 
              "User id=UserName;" + 
              "Password=Secret;"; 
conn.Open();


OleDb -- Trusted Connection
using System.Data.OleDb;
var conn = new OleDbConnection();
conn.ConnectionString = 
              "Driver=SQLOLEDB;" + 
              "Data Source=ServerName;" + 
              "Initial Catalog=DataBaseName;" + 
              "Integrated Security=SSPI;"; 
conn.Open();


OleDb -- via IP Address
using System.Data.OleDb;
var conn = new OleDbConnection();
conn.ConnectionString = 
              "Driver=SQLOLEDB;" + 
              "Network Library=DBMSSOCN;" + 
              "Data Source=xxx.xxx.xxx.xxx,1433;" + 
              "Initial Catalog=DataBaseName;" + 
              "User id=UserName;" + 
              "Password=Secret;"; 
conn.Open();


.NET DataProvider -- Standard Connection
using System.Data.SqlClient;
var conn = new SqlDbConnection();
conn.ConnectionString = 
              "Data Source=ServerName;" + 
              "Initial Catalog=DataBaseName;" + 
              "User id=UserName;" + 
              "Password=Secret;"; 
conn.Open();


.NET DataProvider -- Trusted Connection
using System.Data.SqlClient;
var conn = new SqlConnection();
conn.ConnectionString = 
              "Data Source=ServerName;" + 
              "Initial Catalog=DataBaseName;" + 
              "Integrated Security=SSPI;"; 
conn.Open();


.NET DataProvider -- via IP Address
using System.Data.SqlClient;
var conn = new SqlConnection();
conn.ConnectionString = 
              "Network Library=DBMSSOCN;" + 
              "Data Source=xxx.xxx.xxx.xxx,1433;" + 
              "Initial Catalog=DataBaseName;" + 
              "User Id=UserName;" + 
              "Password=Secret;"; 
conn.Open();




Microsoft Sql Express


.NET Data Provider -- Default Relative Path -- Standard Connection
using System.Data.SqlClient;
var conn = new SqlConnection();
conn.ConnectionString = 
     "Data Source=.\SQLExpress;" + 
     "User Instance=true;" + 
     "User Id=UserName;" + 
     "Password=Secret;" + 
     "AttachDbFilename=|DataDirectory|DataBaseName.mdf;"
conn.Open();


.NET Data Provider -- Default Relative Path -- Trusted Connection
using System.Data.SqlClient;
var conn = new SqlConnection();
conn.ConnectionString = 
     "Data Source=.\SQLExpress;" + 
     "User Instance=true;" + 
     "Integrated Security=true;" + 
     "AttachDbFilename=|DataDirectory|DataBaseName.mdf;"
conn.Open();


.NET Data Provider -- Custom Relative Path -- Standard Connection
using System.Data.SqlClient;
AppDomain.CurrentDomain.SetData(
     "DataDirectory", "C:\MyPath\");
var conn = new SqlConnection();
conn.ConnectionString = 
     "Data Source=.\SQLExpress;" + 
     "User Instance=true;" + 
     "User Id=UserName;" + 
     "Password=Secret;" + 
     "AttachDbFilename=|DataDirectory|DataBaseName.mdf;"
conn.Open();


.NET Data Provider -- Custom Relative Path -- Trusted Connection
using System.Data.SqlClient;
AppDomain.CurrentDomain.SetData(
     "DataDirectory", "C:\MyPath\");
var conn = new SqlConnection();
conn.ConnectionString = 
     "Data Source=.\SQLExpress;" + 
     "User Instance=true;" + 
     "Integrated Security=true;" + 
     "AttachDbFilename=|DataDirectory|DataBaseName.mdf;"
conn.Open();


.NET Data Provider -- Absolute Path -- Standard Connection
using System.Data.SqlClient;
var conn = new SqlConnection();
conn.ConnectionString = 
     "Data Source=.\SQLExpress;" + 
     "User Instance=true;" + 
     "User Id=UserName;" + 
     "Password=Secret;" + 
     "AttachDbFilename=C:\MyPath\DataBaseName.mdf;"
conn.Open();


.NET Data Provider -- Absolute Path -- Trusted Connection
using System.Data.SqlClient;
var conn = new SqlConnection();
conn.ConnectionString = 
     "Data Source=.\SQLExpress;" + 
     "User Instance=true;" + 
     "Integrated Security=true;" + 
     "AttachDbFilename=C:\MyPath\DataBaseName.mdf;"
conn.Open();




Microsoft Access


ODBC DSN
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = "Dsn=DsnName";
conn.Open();


ODBC -- Standard Security
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
    "Driver={Microsoft Access Driver (*.mdb)};" + 
    "Dbq=c:\myPath\myDb.mdb;" + 
    "Uid=Admin;Pwd=;"; 
conn.Open();


ODBC -- Workgroup (System Database)
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
    "Driver={Microsoft Access Driver (*.mdb)};" + 
    "Dbq=c:\myPath\myDb.mdb;" + 
    "SystemDb=c:\myPath\myDb.mdw;"; 
conn.Open();


ODBC -- Exclusive Use
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
     "Driver={Microsoft Access Driver (*.mdb)};" + 
     "Dbq=c:\myPath\myDb.mdb;" + 
     "Exclusive=1;"; 
     "Uid=Admin;Pwd=;"; 
conn.Open();


OleDb with MS Jet -- Standard Security
using System.Data.OleDb;
var conn = new OleDbConnection();
conn.ConnectionString = 
           "Provider=Microsoft.Jet.OLEDB.4.0;" + 
           "Data Source=c:\mypath\myDb.mdb;" + 
           "User id=admin;" + 
           "Password=";
conn.Open();


OleDb with MS Jet -- Workgroup (System Database)
using System.Data.OleDb;
var conn = new OleDbConnection();
conn.ConnectionString = 
           "Provider=Microsoft.Jet.OLEDB.4.0;" + 
           "Data Source=c:\mypath\myDb.mdb;" + 
           "System Database=c:\mypath\myDb.mdw;"; 
conn.Open();


OleDb with MS Jet -- With Password
using System.Data.OleDb;
var conn = new OleDbConnection();
conn.ConnectionString = 
           "Provider=Microsoft.Jet.OLEDB.4.0;" + 
           "Data Source=c:\mypath\myDb.mdb;" + 
           "Database Password=Secret;"
conn.Open();




Oracle


ODBC DSN
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
              "Dsn=DsnName;" + 
              "Uid=UserName;" + 
              "Pwd=Secret;"; 
conn.Open();


ODBC -- New Microsoft Driver
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
           "Driver={Microsoft ODBC for Oracle};" + 
           "Server=OracleServer.world;" + 
           "Uid=UserName;" + 
           "Pwd=Secret;"; 
conn.Open();


ODBC -- Old Microsoft Driver
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
    "Driver={Microsoft ODBC Driver for Oracle};" + 
    "ConnectString=OracleServer.world;" + 
    "Uid=UserName;" + 
    "Pwd=Secret;"; 
conn.Open();


ODBC -- Oracle Driver
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
    "Driver={Oracle ODBC Driver};" + 
    "Dbq=myDataBase;" + // define in tsnames.ora
    "Uid=UserName;" + 
    "Pwd=Secret;"; 
conn.Open();


OleDb -- Microsoft Driver
uusing System.Data.OleDb;
var conn = new OleDbConnection();
conn.ConnectionString = 
              "Driver=MSDAORA;" + 
              "Data Source=ServerName;" + 
              "User id=UserName;" + 
              "Password=Secret;"; 
conn.Open();


OleDb -- Oracle Driver -- Standard Connection
using System.Data.OleDb;
var conn = new OleDbConnection();
conn.ConnectionString = 
              "Driver=OraOLEDB.Oracle;" + 
              "Data Source=ServerName;" + 
              "User id=UserName;" + 
              "Password=Secret;"; 
conn.Open();


OleDb -- Oracle Driver -- Trusted Connection
using System.Data.OleDb;
var conn = new OleDbConnection();
conn.ConnectionString = 
              "Driver=OraOLEDB.Oracle;" + 
              "Data Source=ServerName;" + 
              "OSAuthent=1;";
conn.Open();
// or 
using System.Data.OleDb;
var conn = new OleDbConnection();
conn.ConnectionString = 
              "Driver=OraOLEDB.Oracle;" + 
              "Data Source=ServerName;" + 
              "User id=/" + 
              "Password=;"; 
conn.Open();


.NET DataProvider from Microsoft -- Standard Connection
using System.Data.OracleClient;
var conn = new OracleConnection();
conn.ConnectionString = 
              "Data Source=ServerName;" + 
              "User id=UserName;"; 
              "Password=Secret;"; 
conn.Open();


.NET DataProvider from Microsoft -- Trusted Connection
using System.Data.OracleClient;
var conn = new OracleConnection();
conn.ConnectionString = 
              "Data Source=Servername;" + 
              "Integrated Security=Yes;"; 
conn.Open();


.NET DataProvider from Oracle -- Standard Connection
using Oracle.DataAccess.Client;
var conn = new OracleConnection();
conn.ConnectionString = 
              "Data Source=ServerName;" + 
              "User id=UserName;"; 
              "Password=Secret;"; 
conn.Open();


.NET DataProvider from Oracle -- Trusted Connection
using Oracle.DataAccess.Client;
var conn = new OracleConnection();
conn.ConnectionString = 
              "Data Source=Servername;" + 
              "Integrated Security=Yes;"; 
conn.Open();




IBM DB2


ODBC DSN
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
              "Dsn=DsnName;" + 
              "Uid=UserName;" + 
              "Pwd=Secret;"; 
conn.Open();


ODBC without DSN
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
              "Driver={IBM DB2 ODBC DRIVER};" + 
              "DataBase=DataBaseName;" + 
              "HostName=ServerName;" + 
              "Protocol=TCPIP;" + 
              "Port=PortNumber;" + 
              "Uid=UserName;" + 
              "Pwd=Secret;"; 
conn.Open();


OleDb -- Microsoft Driver
using System.Data.OleDb;
var conn = new OleDbConnection();
conn.ConnectionString = 
           "Driver=DB2OLEDB;" + 
           "Network Transport Library=TCPIP;" + 
           "Network Address=xxx.xxx.xxx.xxx;" + 
           "Package Collection=CollectionName;" + 
           "Initial Catalog=DataBaseName;" + 
           "User id=UserName;" + 
           "Password=Secret;"; 
conn.Open();


OleDb -- IBM Driver
using System.Data.OleDb;
var conn = new OleDbConnection();
conn.ConnectionString = 
            "Driver=IBMDADB2;" + 
            "DataBase=DataBaseName;" + 
            "HostName=ServerName;" + 
            "Protocol=TCPIP;" + 
            "Port=PortNumber;" + 
            "Uid=UserName;" + 
            "Pwd=Secret;"; 
conn.Open();


.NET DataProvider from IBM
using IBM.Data.DB2;
var conn = new Db2Connection();
conn.ConnectionString = 
              "DataBase=DataBaseName;" + 
              "Uid=UserName;" + 
              "Pwd=Secret;" + 
conn.Open();




MySql


ODBC DSN
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
              "Dsn=DsnName;" + 
              "Uid=UserName;" + 
              "Pwd=Secret;"; 
conn.Open();


ODBC -- MyODBC Driver -- local database
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
            "Driver={MySql};" + 
            "Server=localhost;" + 
            "Option=16834;" + 
            "DataBase=DataBaseName;" 
conn.Open();


ODBC -- MyODBC Driver -- remote database
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
            "Driver={MySql};" + 
            "Server=db.domain.com;" + 
            "Option=131072;" + 
            "Port=3306;" + 
            "Stmt=;" + 
            "DataBase=DataBaseName;" + 
            "Uid=UserName;" + 
            "Pwd=Secret;" 
conn.Open();


ODBC -- MySQL ODBC 3.51 Driver
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
     "Driver={MySql ODBC 3.51 Driver};" + 
     "Server=ServerName;" + 
     "Option=16834;" + 
     "Port=3306;" + 
     "Stmt=;" + 
     "DataBase=DataBaseName;" + 
     "Uid=UserName;" + 
     "Pwd=Secret;" 
conn.Open();
// or 
var conn = new OdbcConnection();
conn.ConnectionString = 
     "DRIVER={MySql ODBC 3.51 Driver};" + 
     "SERVER=ServerName;" + 
     "DATABASE=DataBaseName;" + 
     "USER=UserName;" + 
     "PASSWORD=Secret;" 
conn.Open();


OleDb
using System.Data.OleDb;
var conn = new OleDbConnection();
conn.ConnectionString = 
            "Provider=MySqlProv;" + 
            "Data Source=ServerName;" + 
            "User id=UserName;" + 
            "Password=Secret;" 
conn.Open();


.NET DataProvider from CoreLab
using CoreLab.MySql;
var conn = new MySqlConnection();
conn.ConnectionString = 
              "Host=ServerName;" + 
              "DataBase=DataBaseName;" + 
              "Protocol=TCP;" + 
              "Port=3306;" + 
              "Direct=true;" + 
              "Compress=false;" + 
              "Pooling=true;" + 
              "Min Pool Size=0;" + 
              "Max Pool Size=100;" + 
              "Connection Lifetime=0;" + 
              "User id=UserName;" + 
              "Password=Secret;" + 
conn.Open();




Sybase


ODBC DSN
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
              "Dsn=DsnName;" + 
              "Uid=UserName;" + 
              "Pwd=Secret;"; 
conn.Open();


ODBC -- Sybase System 12 (12.5) ODBC Driver
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
              "Driver={SYBASE ASE ODBC Driver};" + 
              "Srvr=ServerName;" + 
              "Uid=UserName;" + 
              "Pwd=Secret;"; 
conn.Open();


ODBC -- Sybase System 11 ODBC Driver
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
           "Driver={SYBASE SYSTEM 11};" + 
           "Srvr=ServerName;" + 
           "Uid=UserName;" + 
           "Pwd=Secret;"; 
conn.Open();


ODBC -- Intersolv 3.10 ODBC Driver
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
        "Driver={INTERSOLV 3.10 32-BIT Sybase};" + 
        "Srvr=ServerName;" + 
        "Uid=UserName;" + 
        "Pwd=Secret;"; 
conn.Open();


ODBC -- SQL Anywhere
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
         "ODBC;" + 
         "Driver={Sybase SQL Anywhere 5.0};" + 
         "DefaultDir=c:\myfolder\;" + 
         "Dbf=c:\mypath\dbname.db;" + 
         "Uid=UserName;" + 
         "Pwd=Secret;" + 
         "Dsn="""";";     // Must be included!
conn.Open();


OleDb -- Sybase Adaptive Server Enterprise (ASE)
using System.Data.OleDb;
var conn = new OleDbConnection();
conn.ConnectionString = 
              "Driver=Sybase.ASEOLEDBProvider;" + 
              "Server Name=ServerName,5000;" + 
              "Initial Catalog=DataBaseName;" + 
              "User id=UserName;" + 
              "Password=Secret;"; 
conn.Open();
// optionally, replace 
// 'Server Name' with 'Srvr', and 
// 'Initial Catalog' with 'Catalog'


.NET DataProvider from Sybase
using Sybase.Data.AseClient;
var conn = new AseConnection();
conn.ConnectionString = 
              "Data Source=ServerName;" + 
              "Initial Catalog=DataBaseName;" + 
              "User id=UserName;" + 
              "Password=Secret;"; 
conn.Open();




Interbase


ODBC DSN
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
              "Dsn=DsnName;" + 
              "Uid=UserName;" + 
              "Pwd=Secret;"; 
conn.Open();


ODBC -- EasySoft ODBC Driver -- local machine
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
      "Driver={Easysoft IB6 ODBC};" + 
      "Server=localhost;" + 
      "DataBase=localhost:C:\MyPath\DbName.gdb;" + 
      "Uid=UserName;" + 
      "Pwd=Secret;"; 
conn.Open();


ODBC -- EasySoft ODBC Driver -- remote machine
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
      "Driver={Easysoft IB6 ODBC};" + 
      "Server=ServerName;" + 
      "DataBase=ServerName:C:\MyPath\DbName.gdb;" + 
      "Uid=UserName;" + 
      "Pwd=Secret;"; 
conn.Open();


ODBC -- Intersolv ODBC Driver -- local machine
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
      "Driver=" + 
   "{INTERSOLV InterBase ODBC Driver (*.gdb)};" + 
      "Server=localhost;" + 
      "DataBase=localhost:C:\MyPath\DbName.gdb;" + 
      "Uid=UserName;" + 
      "Pwd=Secret;"; 
conn.Open();


ODBC -- Intersolv ODBC Driver -- remote machine
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
      "Driver=" + 
   "{INTERSOLV InterBase ODBC Driver (*.gdb)};" + 
      "Server=ServerName;" + 
      "DataBase=ServerName:C:\MyPath\DbName.gdb;" + 
      "Uid=UserName;" + 
      "Pwd=Secret;"; 
conn.Open();




Informix


ODBC DSN -- INFORMIX 3.30 ODBC Driver
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
              "Dsn=DsnName;" + 
              "Host=HostName;" + 
              "Server=ServerName;" + 
              "Service=ServerName;" + 
              "Protocol=olsoctcp;" + 
              "Database=DataBaseName;" + 
              "Uid=UserName;" + 
              "Pwd=Secret;"; 
conn.Open();


ODBC without DSN -- INFORMIX 3.30 ODBC Driver
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
              "Dsn="";" + 
              "Driver={INFORMIX 3.30 32 BIT};" + 
              "Host=HostName;" + 
              "Server=ServerName;" + 
              "Service=ServerName;" + 
              "Protocol=olsoctcp;" + 
              "Database=DataBaseName;" + 
              "Uid=UserName;" + 
              "Pwd=Secret;"; 
conn.Open();


ODBC Informix-CLI 2.5 ODBC Driver
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
          "Driver={Informix-CLI 2.5 (32 Bit)};" + 
          "Server=ServerName;" + 
          "DataBase=DataBaseName;" + 
          "Uid=UserName;" + 
          "Pwd=Secret;"; 
conn.Open();


OleDb -- IBM Informix OleDb Provider
using System.Data.OleDb;
var conn = new OleDbConnection();
conn.ConnectionString = 
        "Driver=IFXOLEDBC;" + 
        "Data Source=DataBaseName@ServerName;" + 
        "User id=UserName;" + 
        "Password=Secret;"; 
        "Persist Security Info=true;"; 
conn.Open();




Excel


ODBC DSN
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
              "Dsn=DsnName;" + 
              "Uid=UserName;" + 
              "Pwd=Secret;"; 
conn.Open();


ODBC without DSN
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
       "Driver={Microsoft Excel Driver (*.xls)};" + 
       "Driverid=790;" + 
       "Dbq=C:\MyPath\SpreadSheet.xls;" + 
       "DefaultDir=C:\MyPath;"; 
conn.Open();


OleDb with MS Jet
using System.Data.OleDb;
var conn = new OleDbConnection();
conn.ConnectionString = 
    "Driver=Microsoft.Jet.OLEDB.4.0;" + 
    "Data Source=C:\MyPath\SpreadSheet.xls;" + 
   @"Extended Properties=""Excel 8.0;HDR=Yes"""; 
conn.Open();
<




Text


ODBC DSN
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
              "Dsn=DsnName;" + 
              "Uid=UserName;" + 
              "Pwd=Secret;"; 
conn.Open();


ODBC without DSN
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
 "Driver={Microsoft Text Driver (*.txt; *.csv)};" + 
 "Dbq=C:\MyPath\;" + 
 "Extensions=asc,csv,tab,txt;"; 
conn.Open();
// Use: sql = "Select * From MyTextFile.txt"


OleDb with MS Jet
using System.Data.OleDb;
var conn = new OleDbConnection();
conn.ConnectionString = 
      "Driver=Microsoft.Jet.OLEDB.4.0;" + 
      "Data Source=C:\MyPath\;" + 
      "Extended Properties=" + 
        @"""text;HDR=Yes;FMT=Delimited"""; 
conn.Open();
// Use: sql = "Select * From MyTextFile.txt"




dBase Dbf


ODBC DSN
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = "Dsn=DsnName";
conn.Open();
// Use: sql = "Select * From MyDb.dbf"


ODBC without DSN
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
     "Driver={Microsoft dBASE Driver (*.dbf)};" + 
     "Driverid=277;" + 
     "Dbq=C:\MyPath\";
conn.Open();
// Use: sql = "Select * From MyDb.dbf"




Visual FoxPro


ODBC DSN
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = "Dsn=DsnName";
conn.Open();


ODBC without DSN -- Database container (dbc)
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
      "Driver={Microsoft Visual FoxPro Driver};" + 
      "SourceType=DBC;" + 
      "SourceDB=C:\MyPath\MyDb.dbc;" + 
      "Exclusive=No"; 
conn.Open();


ODBC without DSN -- Free table directory
using System.Data.Odbc;
var conn = new OdbcConnection();
conn.ConnectionString = 
      "Driver={Microsoft Visual FoxPro Driver};" + 
      "SourceType=DBF;" + 
      "SourceDB=C:\MyPath;" + 
      "Exclusive=No"; 
conn.Open();


OleDb -- Database container (dbc)
using System.Data.OleDb;
var conn = new OleDbConnection();
conn.ConnectionString = 
              "Driver=VFPOLEDB;" + 
              "Data Source=C:\MyPath\MyDb.dbc;" + 
              "Collating Sequence=machine;" + 
              "Password=Secret;"; 
conn.Open();


OleDb -- Free table directory
using System.Data.OleDb;
var conn = new OleDbConnection();
conn.ConnectionString = 
              "Driver=VFPOLEDB;" + 
              "Data Source=C:\MyPath\;" + 
              "Collating Sequence=general;" + 
              "Password=Secret;"; 
conn.Open();
