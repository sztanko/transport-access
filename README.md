transport-access
================

Current project contains data on station accessibility.

That is, for each station in UK I render number of other stations accessible within 30 minutes, 45 minutes and one hour.

Sources
-----------

Primary datasource is open data from Association of Train Operating Companies: http://data.atoc.org/

I also use TFL offline timetables for routing of London Underground, DLR, Tram, Emirates Air Line and ferries. Bus data is not taken into account.

Heritage railways (e.g. Spa Vallery Railway) are not included, as I couldn't find any related open data. If you have that data in machine-readible format, please contact me: sztanko@gmail.com

Neither have I Glasgow Subway timetable included.

All the data is gathered from open sources and is avaialable under Open Government License.

Methodology
-------------

Shortest paths are calculated using Dijkstra algorithm. I am using iGraph and it's python module.
I add extra 2 minutes for entering a station and another 2 minutes for exit. Interchange takes max(1 minute, half of the average waiting time for the next service). I also consider walking from one station to another (only those stations located less then 2 kilometers from each other)

All weekend and weekday services are considered.


The Future
----------

If I will have time, I might create some visualisation on top of this.

If you are interested in some other type of general stats I can extract, please let me know.

Other
-----

Please have a look as http://www.saltaku.com and http://borisbikes.saltaku.com for my other routing related projects.


Credits and Contact
--------------------

Thanks Tom Cairns for CIFReader: https://github.com/swlines/CIFReader and dr. Tamas Nepusz for Igraph: http://igraph.sourceforge.net/

Data contained in this project can be freely reused in any way you wish. If you find any way to cause harm to people using this data, please don't.

My name is Demeter Sztanko, people call me Dimi. You can contact me at sztanko@gmail.com. Also you can follow me on Twitter: @sztanko. I generally tweet about maps and routing.
