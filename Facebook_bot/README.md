# Facebook bot : Flask + AWS Lambda + Zappa
## Bot features
  - Facebook bot sends motivational quotes every n minutes to FB Messanger
  - Responds to questions about local time in city. Example: "Time in New York?"

## Instructions to run code in Docker:
  - Save AWS credentials in keys/credentials and keys/config.<sup>1</sup>

  - Update environmental variables in "docker-compose environment" and "zappa_settings.json"

  - Build docker and image:

        bash script/docker.sh
  
  - Update Facebook Webhook in developers.facebook.com (VERIFY_TOKEN from environ veriables), URL from:
  - Local run from project folder

        ngrok http 5000

  - AWS: zappa deploy URL below

## Instructions to deploy to AWS Lambda:

        docker exec -it fb_bot /bin/bash
        bash script/deploy.sh

## Instructions to update to AWS Lambda:

        docker exec -it fb_bot /bin/bash
        bash script/update.sh

## Sources
<sup>1</sup>[http://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html](http://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html)