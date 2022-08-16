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
web_content_folder
web_content_repo



Dependencies
------------



Example Playbook
----------------

---
- hosts: local
  vars:
    manifest_folder: ~/geogeek_manifests
    gisnamespace: gis
    web_content_folder: ~/geogeeksuite/webcontent
    web_content_repo: git@github.com:GeoGeekSuite/Startpage.git
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

