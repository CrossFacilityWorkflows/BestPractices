.. _Data Transfer:

Data Transfer
=============
This page documents for users how to transfer data between the three ASCR Facilities. In general, instead of using tools like ``scp`` or ``rsync`` for large data transfers, we recommend that data be transferred using `Globus <http://app.globus.org>`_, which is able to transfer data more efficiently and with less user interaction. 

Globus is a service for scheduling data transfers between sites, filling a particular niche among users of large datasets within and between DOE computing facilities and users' home institutions. Instead of synchronously transferring files, users schedule transfers to take place, and the Globus service manages the transfer, recovering as needed from failures, and notifying the user when the transfer completes. In addition to this convenient reliability, transfers over Globus are typically very performant, whether the user is transferring a few very large files, or a large collection of very small files. We also provide details of the Globus endpoints available at each of the ASCR facilities. 

ALCF
~~~~

Users at the ALCF can leverage multiple Globus endpoints for their data transfers, using their ALCF credentials.

+----------------+-----------------------------------------------+-----------------------------+
|  Endpoint Name |               Description                     | Recommended Use             |
+================+===============================================+=============================+
| ALCF Theta     | The main filesystem delivered with Theta.     | Transfers to/from the Theta |
|                |                                               | filesystem at ALCF          |
+----------------+-----------------------------------------------+-----------------------------+
| ALCF Eagle     | Eagle is a new 100 PB filesystem with         | Transfers to/from Eagle     |
|                | additional data sharing functionality exposed | filesystem                  |
|                | through Globus.                               |                             |
+----------------+-----------------------------------------------+-----------------------------+
| ALCF Grand     | Grand is a new 100 PB filesystem.             | Transfers to/from Grand     |
|                |                                               | filesystem                  |
+----------------+-----------------------------------------------+-----------------------------+
| ALCF HPSS      | Tape storage system; for more details, see    | Transfers to/from ALCF      |
|                | link.                                         | tape archive                |
+----------------+-----------------------------------------------+-----------------------------+
     
For more information about Globus sharing using Eagle, see the `related documentation <https://alcf.anl.gov/support-center/theta-and-thetagpu/eagle-data-sharing>`_. 

NERSC
~~~~~
You can log into the Globus web interface with your NERSC credentials (by selecting NERSC in the drop down menu of supported identity providers) 
or using many of the other supported providers listed that you can authenticate against. 
NERSC maintains several Globus endpoints that can be activated for individual use by any NERSC user. 
The list of endpoints is provided in the table below. 


+----------------+-----------------------------------------------+---------------------------+
|  Endpoint Name |               Description                     | Recommended Use           |
+================+===============================================+===========================+
|  NERSC DTN     | Multi-node, high performance transfer system  | Almost all data transfers |
|                | with access to all NERSC Global File          | needs into & out of NERSC |
|                | systems (NGF) as well as Cori Scratch         |                           |
+----------------+-----------------------------------------------+---------------------------+
|   NERSC HPSS   | Single node system connected directly to      | Remote transfers into &   |
|                | the NERSC HPSS tape archive                   | out of HPSS               |
+----------------+-----------------------------------------------+---------------------------+
|  NERSC SHARE   | Single node system with read-only access to   | Shared Globus endpoint    |
|                | some NERSC file systems                       |                           |
+----------------+-----------------------------------------------+---------------------------+
|    NERSC S3    | Single node system with read-only             | Data transfers to  & from |
|                | access to NERSC homes                         | Amazon S3                 |                   
+----------------+-----------------------------------------------+---------------------------+


* Data can be shared at NERSC using `Globus Sharing <https://www.globus.org/data-sharing>`_. Currently shared endpoints are read-only, no writing is allowed. See `this page <https://docs.nersc.gov/services/globus/#sharing-data-with-globus>`_ for more information. 
* NERSC has an experimental Globus S3 endpoint that can be used to access and share content from AWS S3. See `this page <https://docs.nersc.gov/services/globus/#globus-s3-endpoint>`_ for more information. 



OLCF
~~~~

OLCF uses Globus for large bulk transfers into and out of the facility. 
Documentation is available for `transfers from personal computing devices <https://docs.olcf.ornl.gov/data/transferring.html#using-globus-from-your-local-machine>`_ as well as endpoints from one facility to another. 
See `this page <https://docs.olcf.ornl.gov/data/transferring.html>`_ for more information. 

The recommendation to transfer files in and out of OLCF is to begin from the external site, and tar files before executing a transfer between endpoints.


+----------------+-----------------------------------------------+---------------------------+
|  Endpoint Name |               Description                     | Recommended Use           |
+================+===============================================+===========================+
|  OLCF DTN      | Multi-node, high performance transfer system  | Almost all data transfers |
|                | with access to OLCF centewide file system     | needs into & out of OLCF  |
+----------------+-----------------------------------------------+---------------------------+
|   OLCF HPSS    | Single node system connected directly to      | Remote transfers into &   |
|                | the NERSC HPSS tape archive                   | out of HPSS               |
+----------------+-----------------------------------------------+---------------------------+
