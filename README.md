# Instruction
Make a Rails App that can accept GPS waypoints associated to a vehicle, and then show them in a map

# The problem
Write a rails app that can accept GPS waypoints associated to a vehicle, and then show them in a map. 
A GPS waypoint represents a location based on a latitude/longitude pair, and a point in time. 
A vehicle is represented by a unique alphanumeric identifier, and can have multiple GPS waypoints.

Specifically, the app consists of the following endpoints:

- A JSON API endpoint named /api/v1/gps that accepts GPS waypoints associated to a vehicle. The following format must be used:
```json
{
  "latitude": 20.23,
  "longitude": -0.56,
  "sent_at": "2016-06-02 20:45:00",
  "vehicle_identifier": "HA-3452"
}
```
If no vehicle exists with that identifier, create it.

- An HTML endpoint named /show that shows the vehicles' most recent coordinate in a map (choose any map provider you want, such as Google Maps, Open Street Map, Bing Maps, Mapbox, etc.).

# Things to consider
1. All historical waypoints must be stored.
2. No authentication is required for the endpoints.
3. Waypoints received through the API must be processed in a background job processing framework.


# Recommended configuration
- Ruby >= 2.5.2
- Ruby on Rails >= 6
- Postgres database
- Sidekiq
- Redis
- Docker && Docker-Compose
- Google Maps API
