# commande ruby http://guides.rubyonrails.org/command_line.html#rails-dbconsole
FROM ruby

ONBUILD EXPOSE  3000

WORKDIR /opt/app/
RUN apt-get update -y && apt-get install  libpq-dev nodejs gem -y
RUN gem install rails && rails new server && cd server && bundle install\
&& rake db:migrate &&  rake db:seed

WORKDIR /opt/app/server

# run docker build -f Dockerfile -t ft-rails:on-build . 
# dejs
# # to build image
# # then
# # docker build -f ChildDockerfile
