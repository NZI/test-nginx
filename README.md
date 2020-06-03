To test:
 
 - `docker-compose up`
 - visit [http://localhost:8081/](http://localhost:8081/)
    - you should see `7.4.6`
 - visit [http://localhost:8081/error.php](http://localhost:8081/error.php)
    - you should see `7.1.33`
    - logs will show `[warn] 7#7: *2 upstream server temporarily disabled while reading response header from upstream, client: 172.20.0.1, server: localhost, request: "GET /error.php HTTP/1.1", upstream: "fastcgi://172.20.0.4:9000", host: "localhost:8081"`
 - visit [http://localhost:8081/](http://localhost:8081/)
    - you should see `7.1.33`
 - wait 30 seconds
 - visit [http://localhost:8081/](http://localhost:8081/)
    - you should see `7.4.6`