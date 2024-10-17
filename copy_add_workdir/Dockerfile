FROM almalinux
LABEL author="srikanth" \
      company="devops_sol"
EXPOSE 80
RUN dnf install nginx -y 
CMD ["nginx" ,"-g" ,"daemon off;"]
RUN rm -rf /usr/share/nginx/html/* 
COPY index.html /usr/share/nginx/html/index.html
RUN mkdir /tmp/add
WORKDIR /tmp/add
ADD https://expense-builds.s3.us-east-1.amazonaws.com/expense-backend-v2.zip .
