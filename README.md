#Hadoop/Docker-Compose par @Juliopez
## Infrastructure Big Data en utilisant docker-compose.
<br> Cet environnement propose HDFS, Hive, Spark, Hue, Zeppelin, Kafka, Zookeeper et NiFi.
<br> Pour la mise en œuvre de ce conteneur, il suffit de télécharger (cloner) ce référentiel et de procéder à la décompression sur votre machine locale.
<br> Luego, installez la ligne de commande, installez le répertoire Hadoop et utilisez `docker-compose up`
<br>Cela inclut l'installation de Hadoop - HDFS -Spark -Hive- NiFi.
## Nous pouvons vérifier l'exécution correcte du format suivant.
Dans un navigateur, accédez à http://localhost:`numéro de port`

Où peut être <b>numéro de port</b> :

** 50070 (visualiser Hadoop et son NameNode)

** 8080 (Spark Master)

** 8081 (Spark Worker)

** 8888 (Hue. Créer un compte. Identifiez-vous avec « admin » comme utilisateur et « admin » comme mot de passe)

** 9999 (NiFi)

** 3030 (Kafka)

** 18630 ​​(StreamSets. Utiliser « admin »)

** 19090 (Zeppelin)

### Ici, nous sommes en ligne

Exécutez la commande suivante dans la console : `sudo docker exec -it` hive-server bash`

<br> Connectez-vous au répertoire contenant Hive, puis exécutez la commande `cd /opt/hive/bin`
<br> Une fois dans le répertoire, exécutez Hive avec la commande `./hive`

### Veuillez utiliser MySQL

<br> Exécutez la commande suivante dans la console : `sudo docker exec -it database bash`
<br> Exécutez ensuite la commande `mysql -h localhost -u root -p`

<br> Envoyez une requête similaire avec le mot de passe, par exemple : `secret`

### Pour l'utilisation de Spark (Scala)

<br> Exécutez la commande suivante dans la console : `sudo docker exec -it spark-master bash`

<br> Connectez-vous au répertoire contenant Spark, puis exécutez la commande `cd /spark/bin`

<br> Une fois dans le répertoire, Exécutez Hive avec la commande suivante : `./spark-shell`

### Pour l'utilisation de PySpark (Python)

<br> Exécutez la commande suivante dans la console : `sudo docker exec -it spark-master bash`

<br> Connectez-vous au répertoire d'utilisation de Spark avec la commande `cd /spark/bin`

<br> Une fois dans le répertoire, exécutez la commande suivante : `./pyspark`

### Passons à Kafka

<br> Exécutez la commande suivante dans la console : `sudo docker exec -it kafka bash`

<br> Connectez-vous au répertoire contenant le produit et le consommateur Kafka avec la même commande : `cd /usr/local/bin`

<br> Pour créer un TOPIC : `./kafka-topics --create --zookeeper 172.27.1.15:2181` --replication-factor 1 --partitions 1 --topic EJEMPLO`

<br> Pour vérifier la création : `./kafka-topics --list --zookeeper 172.27.1.15:2181`

<br> Pour créer un PRODUCTEUR : `./kafka-console-producer --broker-list localhost:9092 --topic EJEMPLO`

<br> Pour créer un CONSOMMATEUR : `./kafka-console-consumer --bootstrap-server localhost:9092 --from-beginning --topic EJEMPLO`

<br>
<br>
<br> En cas de problème avec HUE, la solution est disponible ici : [https://youtu.be/Ck4sRPa0o24](https://youtu.be/Ck4sRPa0o24)

<br>
<br> Si vous avez besoin d'aide Travaillez avec sqoop, ici une proposition : [https://youtu.be/hLJFzOAbY8Q](https://youtu.be/hLJFzOAbY8Q)
<br>
<br> Plus d'informations dans [Blog de Julio Lopez-Nunez](https://juliopezblog.wordpress.com/).
