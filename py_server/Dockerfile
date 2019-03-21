FROM python:3.5-alpine
ADD . /code
WORKDIR /code
RUN pip install -i https://pypi.tuna.tsinghua.edu.cn/simple -r requirements.txt
CMD ["python", "app.py"]