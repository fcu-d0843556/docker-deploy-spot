FROM python:3.9

WORKDIR /app

WORKDIR /data
RUN git clone https://github.com/donzoe1017/testingBot.git /data/app

WORKDIR /data/app
RUN ls
RUN pip install line-bot-sdk
RUN pip install -r requirements.txt
RUN ls

CMD [ "python", "manage.py", "runserver" ]