FROM python

COPY stocks_products /dj_app

WORKDIR /dj_app

EXPOSE 80

RUN pip install -r /dj_app/requirements.txt

ENV SECRET_KEY django-insecure-nw^y+m^wmxza1asgk+)!ua2qx9)g+#v=6%76-9i8i(6eqiw94j

ENV DEBUG 1

RUN python manage.py migrate

CMD ["gunicorn", "--bind", "0.0.0.0:8000", "stocks_products.wsgi"]