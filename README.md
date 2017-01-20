# Selenium/Protractor in action 

Current status: 

  - Selenium: ![BrowserStack Status](https://www.browserstack.com/automate/badge.svg?badge_key=b0Vwc2NoREppTUk3cC9LS1hXd01ScG93b3JlZVZEdHZQdGZGbnh0bXUzOD0tLTNrZkplL1pPallMSUtBVldsWVpQMEE9PQ==--5c4c2bf17feca5f90d306b7de50d60a6250d3376)
  - Protractor: ![BrowserStack Status](https://www.browserstack.com/automate/badge.svg?badge_key=Q25ibUMrZ2VHVEZMN0FNRFlwS0dMTVRldVNuK09ySDVLMTdCTTdnYW4yRT0tLTFGd3FzNmZvU0tFMkFrRUQrTEZnVEE9PQ==--e3cf740cce60d615649f735b7ac9011b963d9e36)
  - Protractor: ![BrowserStack Status](https://www.browserstack.com/automate/badge.svg?badge_key=KzZPLy9rNS92YmNtenJOczV0UHY0d0VSQWNmYmVodWIxZ3NyZWhOUW93MD0tLUkyS0VPeUpLM09WQlQyUXdkYktmQXc9PQ==--b926906ed6be6744bddeb3348c4c97f87ae6142e)
  - Mocha: ![BrowserStack Status](https://www.browserstack.com/automate/badge.svg?badge_key=UE9OQWJpSWlNWnhLbHZhdElzRE1mdzE2c3BGQU42WTVsbTAwVm13akt1TT0tLXJuSmVxeVpzcXU3YmY1MDE3b3FoRHc9PQ==--32ef88244215b281c50ba7c2054ef134e9ad667d)

This project demonstrates how to test a website with selenium, protractor or mocha. It can test against
browsers on your local machine or remote on [Browserstack](https://www.browserstack.com) and in parallel.

To make it all a bit more challenging, the demo-test site is protected with Basic Authentication :)

In this README I only list the available commands, but for a more in-depth discussion please checkout 
[this](https://scaljeri.github.io/selenium-protractor-browserstack/) article.

#### Run the demo site

    $> docker run -d --name web dockercloud/hello-world
    $> docker run -d -p 80:80 --link web:web --name auth beevelop/nginx-basic-auth

The demo site can be accessed via `http://localhost` with username `foo` and password `bar`

#### Setup
TODO: yarn install, download drivers, selenium jar, Browserstack tunnel, FF 47

#### Local

    $> npm start                                    // nodeJs without selenium - headless
    $> npm start --  --browser firefox              // selenium with Firefox
    $> npm test:mocha -- --browser chrome           // Mocha 
    $> npm test:protractor -- --browser safari      // Protractor
    
TODO: More??

#### Remote

    $> ./BrowserStackLocal --key <key>
    $> npm start -- --browser ie --browser-version=9 --os=windows --os-version=7 --browserstack-user <user> --browserstack-key <key>
    $> npm run test:mocha -- --browser firefox --browsertsack-user <user> --browserstack-key <key> // remote
    $> npm run test:protractor -- --browser firefox --browsertsack-user <user> --browserstack-key <key> // remote
    
TODO: More??
    
#### Selenium standalone

    $> TODO start selenium
    $> npm start -- --browser firefox --selenium-standalone
    
TODO: More??
    
