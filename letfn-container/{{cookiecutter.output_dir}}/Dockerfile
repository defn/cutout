FROM letfn/python

USER app

COPY service /service

ENTRYPOINT [ "/tini", "--", "/service" ]
