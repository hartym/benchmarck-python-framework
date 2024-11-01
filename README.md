# benchmarck-python-framework

The main goal is not to compare framework to each other but to show bottleneck and specificities of each framework.

This is an experiment done in the PyCon sprint. It has no goals to serve as a real benchmark tooling

Each framework should implement:
- A simple API endpoint that return a simple uniq char
- An API endpoint that stock data into the sqlit database
- An API endpoint that retrieve data from a sqlite database
- An API endpoint that return a file of 2MB
- An API endpoint that return a file of 10MB

-------------------- 

Model à utiliser pour la récupération db:

class Post(models.Model):
    pub_date = models.DateField()
    headline = models.CharField(max_length=200)
    content = models.TextField()

The write statement should create elements like:
pub_date = datetime.now()
headline = "Test Perf"
content = "This is the content of the publication"

-----------

Les fichiers à utiliser sont situé à la racine du projet
