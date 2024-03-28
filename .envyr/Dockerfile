
# Envyr Base
FROM python:3.11-alpine

# Base Deps
RUN apk add --no-cache ca-certificates bash build-base linux-headers

# Os Level Deps if any

WORKDIR /envyr/app
# Install Type Specific Deps
ADD ./requirements.txt /envyr/app/requirements.txt
RUN pip install -r requirements.txt

ADD . /envyr/app
ENTRYPOINT ["python", "scan.py"]
