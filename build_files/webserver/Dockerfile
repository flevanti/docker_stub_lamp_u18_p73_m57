FROM flevanti/docker_webserver:u18php73

ARG AWSCLI_ACCESS_KEY
ARG AWSCLI_SECRET_KEY
ARG AWSCLI_DEFAULT_REGION
ARG AWSCLI_OUTPUT_FORMAT

RUN echo "cd /var/www/project" >> ~/.bashrc
RUN mkdir -p ~/.aws
RUN printf "[default]\n" >> ~/.aws/credentials
RUN printf "aws_access_key_id = $AWSCLI_ACCESS_KEY\n" >> ~/.aws/credentials
RUN printf "aws_secret_access_key = $AWSCLI_SECRET_KEY\n" >> ~/.aws/credentials
RUN printf "[default]\n" >> ~/.aws/config
RUN printf "output = $AWSCLI_OUTPUT_FORMAT\n" >> ~/.aws/config
RUN printf "region = $AWSCLI_DEFAULT_REGION\n" >> ~/.aws/config
