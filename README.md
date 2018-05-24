Jetbrains Server
================

This repo contains a playbook for setting up our Jetbrains server which currently hosts [License server](https://www.jetbrains.com/help/license_server/getting_started.html), [Hub](https://www.jetbrains.com/hub/)
and [Upsource](https://www.jetbrains.com/upsource/).

## Installation

1. Order IApp tools server in Basta
2. Install prerequisites
    ```
    sudo yum install ansible git libsemanage-python
    ```
3. Clone and run:
    ```
    HTTPS_PROXY=http://webproxy-utvikler.nav.no:8088 \
      git clone -c http.sslVerify=false \
      https://github.com/navikt/jetbrains-server.git
    
    cd jetbrains-server
    
    ansible-playbook -i inventory setup-playbook.yaml
    ```

4. Continue with the installation of the different products:

### License server
 * Go to [https://jetbrains.adeo.no/licenses](https://jetbrains.adeo.no/licenses) and continue registration.

### Hub
 * Go to [https://jetbrains.adeo.no/hub](https://jetbrains.adeo.no/hub) and continue setup.

### Upsource
 * Go to [https://jetbrains.adeo.no/upsource](https://jetbrains.adeo.no/upsource) and continue setup.
