FROM python:3.9-slim

WORKDIR /cloud

COPY . .

RUN pip install -r requirements.txt

EXPOSE 8080

CMD ["requirements.in", "demo_pb2.py" ; "demo_pb2_grpc.py" ; "logger.py" ; "recommendation_server.py" ; "client.py"]
