FROM python:3.14.0a3-alpine

ENTRYPOINT pytest --flake8 --junit-xml junit.xml
VOLUME ["/mnt"]
COPY requirements.txt constraints.txt /
RUN pip install --no-cache-dir -r requirements.txt -c constraints.txt
WORKDIR /mnt