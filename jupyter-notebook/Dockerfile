FROM continuumio/anaconda3

LABEL maintainer="Wesley Agena"

EXPOSE 8888

# Create working directory
RUN mkdir /opt/notebooks
WORKDIR /opt/conda/bin

# By default, serve site
CMD jupyter notebook --notebook-dir=/opt/notebooks --ip='*' --port=8888 --no-browser --allow-root --bind=0.0.0.0
