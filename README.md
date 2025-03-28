










Part 1: Configure Local AAA Authentication for Console Access on R1
   Step 1: Test connectivity.
    • Ping from PC-A to PC-B.
    • Ping from PC-A to PC-C.
    • Ping from PC-B to PC-C.
    
  Step 2: Configure a local username on R1.
    Configure a username of Admin1 with a secret password of admin1pa55.
    R1(config)# username Admin1 secret admin1pa55
    
  Step 3: Configure local AAA authentication for console access on R1.
    Enable AAA on R1 and configure AAA authentication for the console login to use the local database.
    R1(config)# aaa new-model
    R1(config)# aaa authentication login default local
    
  Step 4: Configure the line console to use the defined AAA authentication method.
    Enable AAA on R1 and configure AAA authentication for the console login to use the default method list.
    R1(config)# line console 0
    R1(config-line)# login authentication default
    
 Step 5: Verify the AAA authentication method.
    Verify the user EXEC login using the local database.
    R1(config-line)# end
    
    %SYS-5-CONFIG_I: Configured from console by console
    R1# exit
    
    R1 con0 is now available Press
    RETURN to get started.
    ************ AUTHORIZED ACCESS ONLY *************
    UNAUTHORIZED ACCESS TO THIS DEVICE IS PROHIBITED.

    User Access Verification

    Username:Admin1
    Password:admin1pa55 R1>

