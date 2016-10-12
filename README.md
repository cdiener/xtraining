## X-training 2016 Materials

Those are the materials for my X-training 2016 mini course

**A practical guide to machine learning**

### Slides

Can be found on SpeakerDeck at https://speakerdeck.com/cdiener/a-practical-guide-to-machine-learning.

### Installation

We will use H2O which is an industrial strength machine learning framework.
It runs on Java so you will need to get install Java first.

On Ubuntu and Debian this can be achieved by running:

```bash
sudo apt-get install default-jre
```

On Windows and Mac download and install by following the instructions
[from here](https://java.com/en/download/).

Following that download H2O [from here](http://h2o-release.s3.amazonaws.com/h2o/rel-turing/8/index.html).

This will give you a zip file which contains `h2o.jar`. Extract and copy
`h2o.jar` to a location you can find easily on your computer.

### Getting the data

Download the data [from here](https://raw.githubusercontent.com/cdiener/xtraining/master/cancer_panels.csv.zip).

There is no need to extract it. Also copy it to a location you can find easily.
I recommend you copy it in the same folder as `h2o.jar`.

### Starting Flow

Flow is the interactive machine learning environment provided by H2O. In order
to start it we will have use a Terminal and change into the folder where
`h2o.jar` resides.

For instance on Mac and Linux if you saved the files in `/home/user/h2o` this
could be done with typing

```bash
cd /home/user/h2o
```

in your Terminal.

On Windows you will have to use the command line. Open the cards view and go
to search and type "cmd" which will help you to open a Terminal. The command
to change folders is still `cd` but you might have to use the drive as well

```
cd C:\folder\folder\h2o
```

You can now start H2O and Flow with typing

```bash
java -jar h2o.jar
```

on Linux and Mac and

```
java.exe -jar h2o.jar
```

on Windows. You can close/terminate H2O and Flow by pressing `Ctrl+c`.

This will start a single multi-core H2O instance with a maximum RAM usage of
1GB. If you want to give more RAM to H2O (faster training) you can do that
using the `-Xmx` flag. For instance to give a maximum of 4GB of RAM:

```bash
java -Xmx4G -jar h2o.jar
```

After H2O has been started and is running you can open you web browser
at http://localhost:54321 to see the H2O Flow interface.
