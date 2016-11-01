# PI Web API Datasource for Grafana

This data source provides access to OSIsoft PI and PI-AF data through PI Web API.

![display](docs/img/system_overview.png)

## Installation

Install using the grafana-cli or clone the repository directly 
into your Grafana plugin directory.

```
grafana-cli pluginx install gridprotectionalliance-osisoftpi-datasource
```

## Usage

Create a new instance of the data source from the Grafana Data Sources
administration page.

It is recommended to use "proxy" access settings.
You may need to add "Basic" authentication to your PIWebAPI
server configuration and add credentials to the data source settings.

NOTE: If you are using PI-Coresight, it is recommended to create a new
instance of PI Web API for use with this plugin.

See [PI Web API Documentation](https://livelibrary.osisoft.com/LiveLibrary/content/en/web-api-v6/) 
for more information on configuring PI Web API.


## Template Variables

Child elements are the only supported template variables.
Currently, the query interface requires a json query.

An example config is shown below.  
`{"path": "PISERVER\\DatabaseName\\ElementNameWithChildren"}`

![template_setup_1.png](docs/img/template_setup_1.png)

## Event Frames and Annotations

This datasource can use AF Event Frames as annotations.

![event-frame](docs/img/event_frame.png)

Creating an annotation query and use the Event Frame category as the query string.
Color and regex replacement strings for the name are supported.

For example:  
![event-frame-setup-1](docs/img/event_frame_setup_1.png)
![event-frame-setup-2](docs/img/event_frame_setup_2.png)  

## Trademarks

All product names, logos, and brands are property of their respective owners.
All company, product and service names used in this website are for identification purposes only.
Use of these names, logos, and brands does not imply endorsement.

OSIsoft, the OSIsoft logo and logotype, and PI Web API are all trademarks of OSIsoft, LLC.