## linux/hardware etc.

    checking for memory hardware on ubuntu

    `sudo lshw -c memory`



## bash -> 
    autocompletion [jak fabryka1 <link>, etc...] -> talk

    https://github.com/ahmetb/kubectx#apt-debian 
    https://github.com/junegunn/fzf - cool highlighint etc.
    as per 
    regex - checking if input is a decimal number...:
    prompt - how to change, so it reflects eg. currently chosen kubectx/?

scripting examples:
    - changing a single line in text file
    [eg. for tar deployments]

regexes:

    regex: check if string is numerical ...
    [[ "$str" =~ ^[0-9]{1,5}$ ]] && echo "yes it is..." 
    if [[ "$str" =~ ^[0-9]{1,5}$ ]]; then echo "yes it is..." ; fi


running scripts in containers.
    - eyaml failing on ubuntu 22.04 -> dockerize (show demo)        
    - failed to load...
        now -> run it in docker.
        how to pass variables / parameters and return the data back? [without having to log into container]

git code:
    - script for finding repos and cloning it somewhere else...



script to analyse:
    https://github.com/rvm/rvm/blob/master/binscripts/rvm-installer





## openssl 3.0:

    - issues with 3.0

    - encyprtion example:
        openssl pkcs12 -info -in <FILE>.p12 -nokeys <-legacy> -clcerts -out <FILEOUT>
        openssl pkcs12 -in <FILENAME>.p12 -nocerts -out <FILE_NAME.key>

    - links/tricks with keys:
        https://www.digicert.com/kb/ssl-support/openssl-quick-reference-guide.htm#:~:text=OpenSSL%20is%20an%20open%2Dsource,certificate%2C%20and%20identify%20certificate%20information.

    - adding a cert (from .pem) file:
        https://ubuntu.com/server/docs/security-trust-store 
        1. Check format if PEM
        sudo apt get install ca-certificates
        sudo cp cert-whatever.pem /usr/local/share/ca-certificates/cert-whatever.crt
        sudo update-ca-certificates
        - what to expect...

    - 

# python radndom

    kids:
         -> creating tree in Turtle [TODOs]
         -> countries-cities map.

    challenges:
        mapping list with lambdas.
        json trtee

    some challanges to discuss:
        #  - regexes
        #  - looking for duplicates in set/list
        #  - processing json -> specifically tree structure (finding parent of...)
        #  - paths -> looking for abs directory/splitting folders/ ?

        exiting from an application:
        code to pass
        argument parameters

    logging:
        log levels.

    preserving order in yaml files:
        https://github.com/wimglenn/oyaml - interesting file https://pypi.org/project/ruamel.yaml/ 


## Software thoughts

good software practices:
    fail-fast approach
        check all permissions, accesses, etc. at the very beginning
        application needs to be as ready as it is possible
        examples:
            checking credentials once container loads
            pulling permissions for a role
            getting attributes of queue/sns/etc

        checking recent errors (if any)
            anything that can potentially fail
    
        dry runs ->
            an app provisioning sthg should be able to run in dry-run mode so:
            that it checks all parameters
            availabiliy of resources
            checks if creation of resources is possible
            checks for potential conflicts.

        backwards compatible entries/parameters:	
            an old running app should be able to work without new parameters
            unless there is a major revision/change in the release process

## Python-y stuff.

    - review scripts from https://matthew-brett.github.io/teaching/index.html 

## AWS notes

    - kinesis: https://www.youtube.com/watch?v=95ZgCv9cnls&feature=youtu.be&ab_channel=theRDnotes 

## Other todos:

    - automated invoicing
    - discuss monitoring of apps:
        - New Relic
        - Flux
        - Cloudwatch
        - Prometheus+Grafana

    