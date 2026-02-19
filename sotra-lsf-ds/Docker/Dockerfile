FROM python:3.9.7

WORKDIR /app

RUN pip config --user set global.progress_bar off
COPY requirements.txt .
RUN pip install -r requirements.txt
RUN pip install youtokentome==1.0.6

COPY sentence_splitter/non_breaking_prefixes /app/sentence_splitter/non_breaking_prefixes

COPY inference_new2.py /app/

CMD ["python3", "inference_new2.py"]
