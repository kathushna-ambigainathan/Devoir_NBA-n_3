# Dockerfile pour le conteneur PySpark
FROM jupyter/pyspark-notebook

# Optionnel : installer des paquets Python supplémentaires
USER root
RUN pip install psycopg2-binary pandas seaborn

# Revenir à l’utilisateur jovyan (celui par défaut de Jupyter)
USER $NB_UID

# Définir un dossier de travail
WORKDIR /home/jovyan/work

# Copier ton code si tu veux
COPY ./notebooks /home/jovyan/work