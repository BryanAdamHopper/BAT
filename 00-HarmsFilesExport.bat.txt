@echo off
REM ##################################################################
REM # Competitor:  Harms Millenium
REM # Description: File Grabber
REM # CreatedBy:   Bryn Hopper
REM #
REM # HowToUse: 	
REM #	- Place this batch file (and 00-DBFPlus.exe) in the same directory as the files you want to copy.
REM #	- Run this batch file.
REM #	- Files will be copied to "HARMSFILES" in this same directory.
REM #	- 00-DBFPlus.exe will open for each DBF file.
REM #	- Click "Export".
REM #	- Ctrl + V (will paste the DBF file's name in the text box).
REM #	- Save As "CSV".
REM #	- On closing DBFPlus, the next DBF will be opened.
REM #	- Repeat for all 12 files.
REM #
REM ##################################################################
mkdir HARMSFILES
copy "%~dp0\CLIENTMISC.DBF" "%~dp0\HARMSFILES\"
copy "%~dp0\CLIENTS.DBF " "%~dp0\HARMSFILES\"
copy "%~dp0\APPOINTDETAIL.DBF" "%~dp0\HARMSFILES\"
copy "%~dp0\SERVICES.DBF" "%~dp0\HARMSFILES\"
copy "%~dp0\EMPINFO.DBF" "%~dp0\HARMSFILES\"
copy "%~dp0\PRODUCTS.DBF" "%~dp0\HARMSFILES\"
copy "%~dp0\DISTRIB.DBF" "%~dp0\HARMSFILES\"
copy "%~dp0\MANUFACT.DBF" "%~dp0\HARMSFILES\"
copy "%~dp0\PRDCLASS.DBF" "%~dp0\HARMSFILES\"
copy "%~dp0\PRDSUBCLASS.DBF" "%~dp0\HARMSFILES\"
copy "%~dp0\TRANSACTION.DBF" "%~dp0\HARMSFILES\"
copy "%~dp0\TRANSHEAD.DBF" "%~dp0\HARMSFILES\"
mkdir CSV
echo CLIENTMISC| clip
"%~dp0\00-DBFPlus.exe" "%~dp0\HARMSFILES\CLIENTMISC.DBF"
echo CLIENTS| clip
"%~dp0\00-DBFPlus.exe" "%~dp0\HARMSFILES\CLIENTS.DBF"
echo APPOINTDETAIL| clip
"%~dp0\00-DBFPlus.exe" "%~dp0\HARMSFILES\APPOINTDETAIL.DBF"
echo SERVICES| clip
"%~dp0\00-DBFPlus.exe" "%~dp0\HARMSFILES\SERVICES.DBF"
echo EMPINFO| clip
"%~dp0\00-DBFPlus.exe" "%~dp0\HARMSFILES\EMPINFO.DBF"
echo PRODUCTS| clip
"%~dp0\00-DBFPlus.exe" "%~dp0\HARMSFILES\PRODUCTS.DBF"
echo DISTRIB| clip
"%~dp0\00-DBFPlus.exe" "%~dp0\HARMSFILES\DISTRIB.DBF"
echo MANUFACT| clip
"%~dp0\00-DBFPlus.exe" "%~dp0\HARMSFILES\MANUFACT.DBF"
echo PRDCLASS| clip
"%~dp0\00-DBFPlus.exe" "%~dp0\HARMSFILES\PRDCLASS.DBF"
echo PRDSUBCLASS| clip
"%~dp0\00-DBFPlus.exe" "%~dp0\HARMSFILES\PRDSUBCLASS.DBF"
echo TRANSACTION| clip
"%~dp0\00-DBFPlus.exe" "%~dp0\HARMSFILES\TRANSACTION.DBF"
echo TRANSHEAD| clip
"%~dp0\00-DBFPlus.exe" "%~dp0\HARMSFILES\TRANSHEAD.DBF"