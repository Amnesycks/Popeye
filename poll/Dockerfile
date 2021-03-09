FROM python
COPY ./ ./home/user/poll
RUN  pip3 install -r /home/user/poll/requirements.txt
EXPOSE 80
WORKDIR /home/user/poll
CMD ["flask", "run", "--host=0.0.0.0", "--port=80"]
