Jetbrains License Server
========================

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
      https://github.com/navikt/jetbrains-license-server.git
    
    cd jetbrains-license-server
    
    ansible-playbook -i inventory setup-playbook.yaml
    ```

4. Go to [https://jetbrains.adeo.no](https://jetbrains.adeo.no) and continue registration.
