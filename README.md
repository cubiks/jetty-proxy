# jetty-proxy
Testing Camel-Jetty component as proxy/bridge to another endpoint

### Build

    mvn clean install

### Run

#### Server

    cd jetty-proxy-server
    mvn camel:run

#### Server

    cd jetty-proxy-bridge
    mvn camel:run

### Deploy [Karaf/Fuse]

    install -s mvn:com.playground.camel/jetty-proxy-server/1.0.0-SNAPSHOT
    install -s mvn:com.playground.camel/jetty-proxy-bridge/1.0.0-SNAPSHOT

### Test

Access:

    http://localhost:7071/withoutTimeout
=> 503 Service Unavailable

Access:

    http://localhost:7071/withTimeout
=> 200 OK!
