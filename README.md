Webhoster
=========

Ansible script to deploy a pod to host static content and downloads in K8S.

Requirements
------------

Running Kubernetes environment.

Role Variables
--------------

manifest_folder
gisnamespace
webhoster
  image
  tag
web_content



Dependencies
------------



Example Playbook
----------------

---
- hosts: local
  vars:
    manifest_folder: ~/geogeek_manifests
    gisnamespace: gis
    webcontent: ~/geogeeksuite/webcontent
    webhoster:
      image: 'httpd'
      tag: '2.4'
  roles:
  - { role: geogeeksuite.webhoster,
        tags: webhoster }

License
-------

Apache License Version 2.0

Author Information
------------------
Created by Marco Bradtke, contact via geogeeksuite.com

