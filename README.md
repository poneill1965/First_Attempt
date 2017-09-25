# First_Attempt
My First git repo
# Added in some robot stuff
*** Settings ***
Library    String
Library    OperatingSystem

*** Test Cases ***
HelloWorld
    Log    Hello, world!

Hello Darwin
    ${darwin_string}=    Set Variable    Darwin Kernel
    ${result}=    Check OS
    Log    ${result}
    Should Contain    ${result}   ${darwin_string}

*** Keywords ***

Check OS
    ${result}=    Run    uname -a
    [Return]    ${result}
