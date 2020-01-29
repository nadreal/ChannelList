======================================================================
           			HLS Streaming server
                    Version 1.0

                    README.txt
======================================================================


Overview
======================================================================
This README.txt file describes how to install and setup
HLS Streaming server.

It consists of the following sections:
   - Definitions
   - Before You Install
   - Extracting the Distribution
   - Installation Instructions
   - Run Server Instructions     
   - Uninstallation Instructions
    
Definitions
======================================================================
Server Host   The host where the HLS streaming server is installed and 
              running. This system must be a Linux host.


Before You Install
======================================================================

To install HLS streaming server to work on host,
python must be installed and configured on the host.

Before installation install flask on host server:

   - sudo apt-get install python-pip

   - sudo pip install flask


Extracting the Distribution File
======================================================================
The HLS streaming server distribution file,

   HLSStreamingServer.tar.gz

must be extracted on a LINUX host before any packages can be installed.

Command for extracting the distribution is:
   
   tar xvf HLSStreamingServer.tar.gz


Installation Instructions
======================================================================
There are two required steps to install this product:

   1. change script permissions: chmod +x install_all.sh
   2. run script: ./install-all.sh


Run Server Instructions
======================================================================

After instalation is completed in the server home directory (HLSStreamingServer directory) will appear folder HLS_STREAMS.

Enter into HLS_STREAMS directory:

	cd HLS_STREAMS

and run script:
        
       ./runServer.sh

This script will start server for live and VOD streaming (both crypted and uncrypted):
	1.for live unencrypted stream playlist can be found at http://<ipaddr>:8082/variant_clear_bip_bop.m3u8
	2.for live unencrypted stream playlist can be found at http://<ipaddr>:8086/variant_clear_steve_jobs.m3u8
  3.for live unencrypted stream playlist can be found at http://<ipaddr>:8090/variant_clear_bunny.m3u8
	4.for live encrypted stream playlist can be found at http://<ipaddr>:8084/variant_encrypted_bip_bop.m3u8
	5.for live encrypted stream playlist can be found at http://<ipaddr>:8088/variant_encrypted_steve_jobs.m3u8
  6.for live encrypted stream playlist can be found at http://<ipaddr>:8092/variant_encrypted_bunny.m3u8
	7.for VOD unencrypted stream playlist can be found at http://<ipaddr>:8082/static/VOD/bipbop_4x3_clear/bipbop_4x3_variant.m3u8
  8.for VOD unencrypted stream playlist can be found at http://<ipaddr>:8086/static/VOD/SteveJobs_clear/SteveJobs.m3u8
  9.for VOD unencrypted stream playlist can be found at http://<ipaddr>:8090/static/VOD/SteveJobs_clear/bunny.m3u8
	10.for VOD encrypted stream playlist can be found at http://<ipaddr>:8084/static/VOD/bipbop_4x3_encrypted/bipbop_4x3_variant.m3u8
  11.for VOD encrypted stream playlist can be found at http://<ipaddr>:8088/static/VOD/SteveJobs_encrypted/SteveJobs_variant.m3u8
  12.for VOD encrypted stream playlist can be found at http://<ipaddr>:8092/static/VOD/SteveJobs_encrypted/bunny_variant.m3u8

	where <ipaddr> is IP address of the host.

To stop running servers press ENTER in terminal where servers are running and  then run script:
      
        ./stopServer.sh


Uninstall Server Packages
----------------------------------------------------------------------
To uninstall HLS streaming server just simply remove HLS_STREAMS directory

