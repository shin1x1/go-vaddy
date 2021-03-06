
go-vaddy: VAddy API Command-Line Tool
=================================

VAddy API Command-Line Tool using golang  
https://vaddy.net

Go-vaddy can start scan and check the result.

## OS type

You can use exe files on `go-vaddy/bin` directory.
If you use linux(64bit), use vaddy-linux-64bit.  

For example, `./vaddy-linux-64bit  api_key userID FQDN`

| OS            | file               |
| ------------- |:------------------:|
| Linux(64bit)  | vaddy-linux-64bit  |
| MacOS(64bit)  | vaddy-macosx-64bit |
| Windows(64bit)| vaddy-win-64bit.exe|
| FreeBSD(64bit)| vaddy-freebsd-64bit|
| Linux(32bit)  | vaddy-linux-32bit  |
| Windows(32bit)| vaddy-win-32bit.exe|
| FreeBSD(32bit)| vaddy-freebsd-32bit|



## Usage (start scan and get the result)

### Exit status
Go-vaddy returns 0 (no errors, no vulnerabilities) or 1 (errors, 1 or more vulnerabilities).




### ENV
You can check V1/V2 project on the dashboard screen after login.

#### for V1 Project

    export VADDY_TOKEN="123455667789"  
    export VADDY_USER="ichikaway"  
    export VADDY_HOST="www.examplevaddy.com"  
    #export VADDY_CRAWL="30"

#### for V2 Project

    export VADDY_TOKEN="123455667789"
    export VADDY_USER="ichikaway"
    export VADDY_PROJECT_ID="your project id"
    #export VADDY_CRAWL="30"

`VADDY_CRAWL` is optional. If you don't specify it, VAddy uses the latest crawl data.  
You can specify crawl label keyword on `VADDY_CRAWL` like this  

    export VADDY_CRAWL="search result pages"  

### Command Execution

    cd bin
    ./vaddy-linux-64bit


### Slack Integration
Setting these OS environment variables,
Post message to the slack when VAddy found vulnerabilities.  

    export SLACK_WEBHOOK_URL="webhook url"
    export SLACK_USERNAME="your user (optional)"
    export SLACK_CHANNEL="your channel (optional)"
    export SLACK_ICON_EMOJI=":smile: (optional)"
    export SLACK_ICON_URL="icon url (optional)"
