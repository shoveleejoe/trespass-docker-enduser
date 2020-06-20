FROM sameersbn/redmine:2.5.0

RUN rm -R /redmine/plugins/*

WORKDIR /redmine/plugins/

RUN git clone https://github.com/brandonaaron/redmine_rubycas.git

RUN chown -R www-data:www-data /redmine/plugins/

WORKDIR /redmine/

COPY init-sql.sh /init-sql.sh

RUN chmod +x /init-sql.sh

RUN bundle install
