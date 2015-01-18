[![Build Status](https://travis-ci.org/wzrdtales/node-ultimate-migrate.svg?branch=master)](https://travis-ci.org/wzrdtales/node-ultimate-migrate) 
[![Documentation Status](https://readthedocs.org/projects/umigrate/badge/?version=latest)](https://readthedocs.org/projects/umigrate/?badge=latest)

# Ultimate Migrate

Umigrate is a extendable X Language and X Database Migration, Migration generation and Database difftool.

#Starter Guide

Follow this path in the following order, to get known to umigrate:

  1. [Configuration](http://umigrate.readthedocs.org/en/latest/usage/configuration/)
  2. [Getting Started](http://umigrate.readthedocs.org/en/latest/usage/getting%20started/)

## Goals

 * Completely independent from the Database used (X Database)

I want to be able to switch between Databases at any time, without having to care about compatibility of the existing Migrations.

 * Completely independent from the Migrator used (X Language)

I want to be able to use a different Migrator (for example Laravel Migrations).
 * Support of all specific and standard features of Databases
 * No need for writing Migrations manually, unless non deterministic actions have been done (renaming)