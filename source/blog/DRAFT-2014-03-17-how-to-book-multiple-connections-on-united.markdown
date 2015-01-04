---
title: How to Book Multiple Connections on United.com
---

Somewhat recently, some dissapointing news arose that United.com is no longer showing multiple-connection itineraries by default. 
For most people, this is probably a useful default, but it can pose a problem for mileage runners and others who deliberately want multiple connections, 
or want to force a connection somewhere.

Typically when I compose a mileage run, I do up-front research and determination of routes using ITA Matrix, then go over to United.com to find the same route. 
While sometimes this isn't possible when booking a round trip, usually it's at least possible with two one-way fares. 
With the new restriction in place, this may not be possible for some routes. So how do you book multiple-connection itineraries on United?

The first thing to remember is that ITA Matrix will show a pretty comprehensive
set of routings valid per the *fare rules*, but nothing is direclty bookable on
ITA.

After doing up-front research on ITA Matrix, **search for the flight in Hipmunk**.
Hipmunk is actually built on ITA Matrix and you can enter advanced routing codes after the source and destination airport codes by adding them after "::". 
You'll see upon typing this that Hipmunk even gives a drop-down of useful codes (which is by no means exhaustive).

So for example if you wanted to book a flight SAN-SFO-EWR-PHL (as I did recently) even though that routing doesn't show on United.com, go to Hipmunk and search as follows:

  Source: SAN::LAX ORD
  Destination: PHL::ORD LAX

These routing codes after the "::" instruct Hipmunk to only show routes with both LAX and ORD as connection points, 
and effectively "force" the routing to one of the options you can see on ITA Matrix (and therefore know is valid per the fare rules).

After getting the results, you should get a "Book" deep link to book directly to United.com which should take you right to the purchase page with the routing you wanted,
effectively circumventing searching for this particular routing (and failing) on United.com.

Now, the above example effectively filters the connection to only those
airports, but doesn't restrict on airline at all. In the above example, that
very well may show American Airlines flights even if you intended on searching
only United routings. 

You can expand the advanced routing codes further by specifying airline code
between the airports, like this:

  Source: SAN::UA LAX UA ORD UA
  Destination: PHL::UA ORD UA LAX UA

The basically says, "search for all outbound flights with one leg on united to
LAX, another leg on United to ORD, and another leg on United (to destination
PHL)". That should give you back exactly what you want.

You can get even *more* specific by plugging in actual flight numbers which
should always give you back one option. For example:

  Source: SAN::UA111 LAX UA112 ORD UA113

In that case, the airport code is optional, since you're feeding it specific
flights, so you could have just done:

  Source: SAN::UA111 UA112 UA113

