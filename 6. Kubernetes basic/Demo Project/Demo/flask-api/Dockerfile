FROM python:3.12-alpine
COPY . /app
WORKDIR /app
# RUN pip install -r requirements.txt
RUN pip install --no-cache-dir -r requirements.txt
ENV PORT 5000
EXPOSE 5000
ENTRYPOINT [ "python" ]
CMD [ "app.py" ]