FROM python:3.7

RUN pip install Flask python-dotenv
RUN apt-get update && apt-get install -y libhyperscan5 libpq-dev

# Install Credential Digger
RUN pip install credentialdigger

ARG path_model
ARG snippet_model

COPY . /credential-digger-ui
WORKDIR /credential-digger-ui/
RUN chmod +x run.sh
CMD [ "./run.sh" ]
