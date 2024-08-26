# Project Setup with Ddev

This guide provides instructions for setting up a Drupal project using Ddev and running Gulp within the theme directory.

## Table of Contents

1. [Prerequisites](#prerequisites)
2. [Project Setup](#project-setup)
3. [Running Gulp](#running-gulp)
4. [Performance and Core Web Vitals](#performance-and-core-web-vitals)
5. [Troubleshooting](#troubleshooting)

## Prerequisites

Before you begin, ensure you have the following installed:

- [Docker](https://www.docker.com/get-started)
- [Ddev](https://ddev.readthedocs.io/en/latest/#installation)
- [Node.js](https://nodejs.org/) (includes npm)

## Project Setup

1. **Clone the Project Repository**

   git clone https://github.com/gauravmahlawat/drupal-design
   cd dp-assignment

2. **Start Ddev**

   Initialize and start the Ddev environment:

   ddev start

3. **Install Drupal Dependencies**

   Access the Drupal container and install the required dependencies:

   ddev ssh
   composer install

4. **Import Database (if applicable)**

   If you have a database dump, import it using:

   drush sql-cli < digital.sql


## Running Gulp

1. **Navigate to the Theme Directory**

   cd web/themes/custom/digital

2. **Install Gulp Dependencies**

   Ensure you have all the required Gulp dependencies installed:

   npm install

3. **Run Gulp**

   Start the Gulp tasks:

   npm run gulp

   or 

   gulp

   or 

   gulp watch

## Performance and Core Web Vitals

To ensure your Drupal site performs well and meets core web vitals, review the following:

- **Performance Screenshot**

  ![Performance Screenshot](path/to/performance-screenshot.png)

## Troubleshooting

- **Ddev Issues**

  - Ensure Docker is running and properly configured.
  - Check Ddev logs using ddev logs.

- **Gulp Issues**

  - Verify Gulp dependencies are correctly installed.
  - Ensure you have the correct Node.js version.

For more detailed troubleshooting, refer to the Ddev Documentation (https://ddev.readthedocs.io/) and Gulp Documentation (https://gulpjs.com/docs/en/getting-started/quick-start).
