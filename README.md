# Ireland Area Latitude and Longitude Data

This repository contains a collection of JSON files that list the latitude and longitude coordinates for various areas, cities, and towns in the island of Ireland. The data is organized by the names of counties, making it easy to access location information for different regions.

## Backstory
I wanted to make browsing through [adverts.ie](https://www.adverts.ie/) easier for me to tell how far is a listing from my location.  
The name of the areas were collected from Adverts then I used Google Maps API Geocoding to get further info about the area.

This repo is used in a browser extension that shows you how far is an address on Adverts: [https://github.com/housamz/adverts-distance](https://github.com/housamz/adverts-distance)

## Data Format

The JSON files follow a specific format for each entry, representing a specific area within a county. Each entry consists of the following fields:

```json
{
  "area_id": 3593,
  "area_name": "Salthill",
  "county_name": "Galway",
  "county_id": 19,
  "address_components": [
    {
      "long_name": "Galway",
      "short_name": "Galway",
      "types": ["locality", "political"]
    },
    {
      "long_name": "County Galway",
      "short_name": "G",
      "types": ["administrative_area_level_1", "political"]
    },
    {
      "long_name": "Ireland",
      "short_name": "IE",
      "types": ["country", "political"]
    }
  ],
  "formatted_address": "Galway, Ireland",
  "geometry": {
    "bounds": {
      "northeast": {
        "lat": 53.31947049999999,
        "lng": -8.9548057
      },
      "southwest": {
        "lat": 53.2483525,
        "lng": -9.1426873
      }
    },
    "location": {
      "lat": 53.274001,
      "lng": -9.051266199999999
    },
    "location_type": "APPROXIMATE",
    "viewport": {
      "northeast": {
        "lat": 53.31947049999999,
        "lng": -8.9548057
      },
      "southwest": {
        "lat": 53.2483525,
        "lng": -9.1426873
      }
    }
  },
  "place_id": "ChIJ_1stWpWTW0gRgVJJCkQbKwM",
  "types": ["locality", "political"]
}
```

- `area_id`: An identifier for the area as used in Adverts.
- `area_name`: The name of the area, city, or town.
- `county_name`: The name of the county the area belongs to.
- `county_id`: An identifier for the county as used in Adverts.
- `address_components`: An array containing address components for the area, such as locality, administrative area level 1, and country.
- `formatted_address`: The formatted address of the area, typically including locality and country.
- `geometry`: Contains geographical information about the area, including bounds, location, location type, and viewport.
- `place_id`: A unique identifier for the area according to the Google Places API.
- `types`: An array of types describing the area, e.g., "locality" and "political."

## County-wise Data

The data is:
1. Fully included in the file "All.json"
2. Divided into separate JSON files, each corresponding to a specific county in Ireland. The files are named in the format `<county_name>.json`, containing entries for the areas within that county.

## Example Usage

To access the data for a specific county, simply open the corresponding JSON file. For instance, to retrieve the latitude and longitude of areas within Galway, you can refer to the `Galway.json` file. The data can be used for various purposes, such as mapping applications, geographical analysis, or any project that requires location-based information.

## Contributing

If you have additional data or spot any inaccuracies, you are welcome to contribute to this repository. Simply fork the repository, make your changes, and submit a pull request. Please ensure that the data is accurate and follows the established JSON format.

## License

This dataset is provided under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/). You are free to share and adapt the data for any purpose, provided you give appropriate credit to the original contributors.

## Disclaimer

While efforts have been made to ensure the accuracy of the data, there might be errors or outdated information. The contributors and maintainers of this repository disclaim any responsibility for the usage of this data and recommend users to cross-verify with reliable sources before making any critical decisions based on the data.
