# Cominvent's Solr Package repository

This repo contains a single [repository.json](repository.json) file and a public key for all 
Solr plugins from Cominvent. Each plugin will live in other git repositories, but they all
tie in to this same repository.

## Setting up the repository

1. Start Solr with package manager enabled

       # You need to set Java property 'enable.packages=true', e.g.
       bin/solr -c -Denable.packages=true

2. Install this plugin repository into your Solr cluster

       bin/solr package add-repo cominvent https://raw.githubusercontent.com/cominvent/solr-plugins/master

## Installing packages

To list available packages in this repository, run

    bin/solr package list-available

To install a particular package, run

    bin/solr package install <package-name>
    bin/solr package deploy <package-name> -y <collection-name>

To uninstall a pacakge, run

    bin/solr package undeploy <package-name>

See https://solr.apache.org/guide/8_8/package-manager.html for official documentation