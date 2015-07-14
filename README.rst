********************************
ERNe: Evolving Reaction Networks
********************************

**ERNe** (**E**\ volving **R**\ eaction **Ne**\ tworks) is an efficient derivative of the `NEAT algorithm <http://www.cs.ucf.edu/~kstanley/neat.html>`_ directed at the evolution of **biochemical systems** or **molecular programs**. 

ERNe's original paper was published in `IEEE Transactions on Evolutionary Computation <http://dx.doi.org/10.1109/TEVC.2014.2326863>`_

.. contents::
    :local:
    :depth: 1
    :backlinks: none

=============
System requirements
=============

Java 8 (JRE, JDK)

=============
Quick start
=============

1. Clone the repository

.. code-block:: bash

    $ git clone https://github.com/huystalker/evolving-reaction-networks
    $ cd evolving-reaction-networks
    
2. Build with `Gradle <https://gradle.org/>`_:

.. code-block:: bash

    $ ./gradlew dist
    $ cd build/dist
    
3. Run the example:

.. code-block:: bash

    $ ./start.sh use.math.square.RunSquare
    
4. Result files will be generated inside ``result/`` directory. To display result of a run:

.. code-block:: bash

    $ ./start.sh erne.ResultReader <path_to_result>
    
=============
Run on a cluster
=============
1. Edit `Hazelcast <http://hazelcast.org/>`_ configuration file located at ``dist/config/hazelcast.xml`` to specify the computational nodes' IP addresses.

.. code-block:: bash

    $ vi config/hazelcast.xml

2. Copy ``dist`` directory to each node.
3. Start the computational service at each node (excluding the main node):

.. code-block:: bash

    $ cd dist
    $ ./start.sh
    
4. Run the example at the main node:

.. code-block:: bash

    $ ./start.sh use.math.square.RunSquare
    
=============
Development
=============
-------------------
Create Eclipse project
-------------------
.. code-block:: bash

    $ ./gradlew eclipse
    
-------------------
Create IntelliJ project
-------------------
.. code-block:: bash

    $ ./gradlew idea