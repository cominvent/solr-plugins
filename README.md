# Github based Solr Plugins repository

Demo for a GitHub Solr plugin repository.

This repo contains a single [repository.json](repository.json) file and a public key for all 
Solr plugins from Cominvent. Each plugin will live in other git repositories, but they all
tie in to this same repository.

To add this repository to your Solr cluster, run

    bin/solr package add-repo cominvent https://raw.githubusercontent.com/cominvent/solr-plugins/master/repository.json

To list available packages, run

    bin/solr package list-available

To install a particular package, run

    bin/solr package install <package-name>
    bin/solr package deploy <package-name> -y <collection-name>

To uninstall a pacakge, run

    bin/solr package undeploy <package-name>

See https://solr.apache.org/guide/8_8/package-manager.html for official documentation