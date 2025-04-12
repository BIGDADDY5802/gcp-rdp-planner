===========================================
  GCP Lab Planner: RDP Access to Public VM
  Accessing Private Web App via Tags
===========================================

LINKS:

https://cloud.google.com/compute/docs/machine-resource

https://cloud.google.com/about/locations#europe

https://github.com/Gwenbleidd32/startup-script-template


===========================================

STUDENT NAME: 

DATE: 4/5/2025

======================
 1. Project Information
======================

GCP Project ID: 


===========================
 2. Subnet & Network Design
===========================

VPC Network Name: 

Subnet Name: 

CIDR Range (e.g. 10.0.0.0/24): 

Subnet Region: 

Are the public and private instances in the same subnet? (Y/N): ____


=================================
 3. Virtual Machines Configuration
=================================


▶ Windows VM (RDP target)
---------------------------------

VM Name: 

Machine Type (e.g. e2-medium): 

Firewall Tag (e.g. allow-rdp): 


▶ Private Application VM
---------------------

VM Name: 

Machine Type (e.g. e2-small): 

Firewall Tag (e.g. allow-http):


==========================
 4. Firewall Rules Planning
==========================


▶ Firewall Rule to Allow RDP to Windows VM
---------------------------------

Name: 

Direction: INGRESS

Source IP Range:

Protocols/Ports:

Target Tags: 


▶ Rule to Allow HTTP Access to Private VM from Bastion
-------------------------------------------------------

Name: 

Direction: INGRESS

Source Tags or IP Ranges: 

Protocols/Ports: 

Target Tags: 


==============================
 5. Expected Behavior Checklist
==============================

[ ] Can RDP into public instance from local machine?
[ ] Can access private instance’s web app via HTTP from bastion?
[ ] Private instance is NOT accessible directly from internet?

======================
 6. Notes & Observations
======================

======================
 7. cloudnat
======================

Name:

======================
 8. instance templates
======================

Name:

======================
 9. load balancer
======================

Name:

Network tag:

======================
 8. instance groups
======================

Name:

heathcheck: 

scope: 

after instances are provisioned make sure you see your tag in an instance

▶ Firewall Rule
---------------------------------

Source Tags: 

Protocols/Ports: tcp/ 80

Source IP Range: 0.0.0.0/0

======================
 8. load balancer
======================

Name:

frontend: 

proxy-only-subnet: >name< >subnet<

leave ip address as ephemeral. >done<

backend:


______________________________________________________
______________________________________________________
______________________________________________________
