FROM node:12-alpine
COPY ./ ./home/user/result
EXPOSE 80
WORKDIR /home/user/result
RUN npm install
CMD ["node", "server.js"]
