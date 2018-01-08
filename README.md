# Howdy #
This is a place for me to collect and collate interesting articles related to distributed systems, algorithms, tooling, etc.

## Distributed Systems ##
* [Apache Kafka, Samza, and the Unix Philosophy of Distributed Data](http://www.confluent.io/blog/apache-kafka-samza-and-the-unix-philosophy-of-distributed-data) by [Martin Kleppmann](https://twitter.com/martinkl) - a very good introduction to the [Samza](https://samza.apache.org/)/[Kafka](https://kafka.apache.org/) approach to stream processing with particular attention to how this approach relates to the Unix philosophy of small, stand-alone, interchangable tools.  
* [Personalized Recommendations at Etsy](https://codeascraft.com/2014/11/17/personalized-recommendations-at-etsy/) by [Robert Hall](https://codeascraft.com/author/rhall/) of [Esty](https://www.etsy.com/).  Excellent post that summarizes in reasonable detail the approach that Etsy takes in generating recommendations from products to its customers.  This post complements [Conjecture](https://github.com/etsy/Conjecture), Etsy's framework for these recommendations. Strongly suggested for those interested in learning about recommender systems or applied linear algebra.
* [The world beyond batch: Streaming 101](http://radar.oreilly.com/2015/08/the-world-beyond-batch-streaming-101.html) by [Tyler Akidau](http://twitter.com/takidau). A medium length introduction the fundamental concepts of stream processing by one of the authors of Google's in-house solution, [MillWheel](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/41378.pdf).  This is an excellent introduction for those completely new to stream processing. The two biggest take-aways are that stream processing systems that do not provide a consistent view of the data should not be trusted and that for time-based computation, event-time windows, while the most difficult to achieve, are the only approach worth pursuing.


## Performance
* [You're probably wrong about caching](http://msol.io/blog/tech/youre-probably-wrong-about-caching/) by [Mike Solomon](https://twitter.com/msol).  Good summary of potential downsides of using caching to increase system performance.

## Machine learning platforms
* [TFX: A TensorFlow-Based Production-Scale Machine Learning Platform](http://stevenwhang.com/tfx_paper.pdf). Paper from KDD 2017 describing the machine learning platform that Google built.  Includes godo descriptions of how to define a good model, metrics to compare different sets of training data and a high description of API used to deploy into the system.
* [Meet Michelangelo: Uber’s Machine Learning Platform](https://eng.uber.com/michelangelo/). Blog post from Uber describing the platform they've built atop Samza, HDFS, Kafka and TensorFlow.

## Location/GIS
* [How We Built Uber Engineering’s Highest Query per Second Service Using Go](http://eng.uber.com/go-geofence/).  While primarily about why Uber chose Go for their core location geofencing lookup service, this blog post also has some interesting details about how they strucutured the geofences for optimized lookups and how they deliver updated geofences to the running appliction.
