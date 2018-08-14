# ERNe: Evolving Reaction Networks

ERNe (Evolving Reaction Networks) is an efficient derivative of the [NEAT algorithm](http://www.cs.ucf.edu/~kstanley/neat.html) directed at the evolution of biochemical systems or molecular programs.

ERNe's original paper was published in [IEEE Transactions on Evolutionary Computation](http://dx.doi.org/10.1109/TEVC.2014.2326863).

# System requirements

Java 8 (JRE, JDK)

# Quick start

## Build with Gradle

```
./gradlew dist
```

## Run the example

```
cd build/dist
./start.sh use.math.square.RunSquare
```

## Result files will be generated inside result/ directory. To display result of a run

```
./start.sh erne.ResultReader <path_to_result>
```

# Run on a cluster

* Modify Hazelcast configuration to specify the computational nodes' IP addresses

```
vi config/hazelcast.xml
```

* Copy `dist` directory to each node.

* Start the computational service at each node (excluding the main node):

```
cd dist/
./start.sh
```

* Run the example at the main node:

```
./start.sh use.math.square.RunSquare
```

# Development

## Create Eclipse project

```
./gradlew eclipse
```

## Create IntelliJ project

```
./gradlew idea
```
