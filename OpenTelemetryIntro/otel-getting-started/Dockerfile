FROM python:3.8

ADD app.py /

RUN pip install flask

RUN pip install opentelemetry-distro

RUN opentelemetry-bootstrap -a install

CMD opentelemetry-instrument \
    --traces_exporter console \
    --metrics_exporter console \
    flask run --host=0.0.0.0 


