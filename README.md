# An Example ETL Pipeline With Airflow

In this blog post I want to go over the operations of data engineering called Extract, Transform, Load (ETL) and show how they can be automated and scheduled using <a href="https://airflow.incubator.apache.org/">Apache Airflow</a>. You can see the source code for this project <a href="https://github.com/mdh266/AirflowDataPipeline">here</a>.


*Extracting* data can be done in a multitude of ways, but one of the most common ways is to query a <a href="https://en.wikipedia.org/wiki/Web_API">WEB API</a>.  If the query is sucessful, then we will receive data back from the API's server. Often times the data we get back is in the form of <a href="https://en.wikipedia.org/wiki/JSON">JSON</a>.  JSON can pretty much be thought of a semi-structured data or as a dictionary where the dictionary keys and values are strings.  Since the data is a dictionary of strings this means we must *transform* it before storing or *loading* into a database. Airflow is a platform to schedule and monitor workflows and in this post I will show you how to use it to extract the daily weather in New York from the <a href="https://openweathermap.org/api">OpenWeatherMap</a> API, convert the temperature to Celsius and load the data in a simple <a href="https://www.postgresql.org/">PostgreSQL</a> database.


## Requirements

<a href="https://airflow.incubator.apache.org/">Airflow</a>

<a href="https://www.python.org/">Python 2.7</a>

<a href="https://www.postgresql.org/">PostgreSQL</a>

<a href="http://initd.org/psycopg/">psycopg2</a>

<a href="https://www.sqlalchemy.org/">SQLAlchemy</a>

<a href="https://sqlalchemy-utils.readthedocs.io/en/latest/">SQLAlchemy-Utils</a>

To install the requirements (except for Python and postgres) type:

	pip install -r requirements.t

You can see the actual blog post <a href="http://michael-harmon.com/blog/AirflowETL.html">here</a>.