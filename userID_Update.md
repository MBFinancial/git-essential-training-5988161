----**************************************************
----DB_OPs
----HamptonM 260625
----INC 149494
----DEV
----Server: SQL06TA
----DB: IPACS
 
----dbo.FAC_USER
----DBO.FAC_USER_RESPONSIBILITY 

----**************************************************
--Update USER ID from 177 to 276 
select * from [dbo].[FAC_USER_RESPONSIBILITY] where USER_ID = 177 --276
select * from [dbo].[FAC_USER] where USER_ID = 177  --276
select * from [dbo].[SEC_USER] where USER_ID = 177  --276

--BACKUP initial state
--SELECT *
----INTO scratch.dbo.fac_userINC149494
--FROM [dbo].[FAC_USER] 

--BACKUP initial state
--SELECT *
--INTO scratch.dbo.fac_userRESPONSIBILITYINC149494
--FROM [dbo].FAC_USER_RESPONSIBILITY


/*
--1&2
--To Be Changed
SELECT *  
FROM [dbo].[FAC_USER] AS U WITH(NoLock)
WHERE U.[USER_ID] = 177
 
----PROD: SQL05A 3/2 3PM (This will be modified to 295) 881 Rows
 
SELECT *  
FROM [dbo].[FAC_USER] AS U WITH(NoLock)
WHERE U.[USER_ID] = 276

--To Be Changed
SELECT *  
FROM [IPACS].[dbo].[FAC_USER_RESPONSIBILITY] AS R WITH(NoLock)
WHERE R.[USER_ID] = 177
 
----PROD: SQL05A 3/2 3PM (This will be modified to 295) 880 Rows
 
SELECT *  
FROM [IPACS].[dbo].[FAC_USER_RESPONSIBILITY] AS R WITH(NoLock)
WHERE R.[USER_ID] = 276

