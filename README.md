# CDR Mapper

An application that plots towers from call detail record (CDR) data to a map file (kml). It can be used to assist users conducting historical cell site and sector analysis.

Currently it accepts CDR data where the cell sites / towers and CDRs are provided in separate files or where they are in the same row, but where the cell site identifiers are unique to a single network element. See 'future goals' for expansion plans for additional types of data.

This branch uses `easy_gui v0.97` to provide a simple GUI interface. [The master branch](https://github.com/danzek/cdr-mapper/tree/master) is a Flask web application.

I have uploaded [a Windows installer](https://github.com/danzek/cdr-mapper/tree/gui/installer) for the GUI branch.

## License

[MIT](https://github.com/danzek/cdr-mapper/blob/master/LICENSE), Copyright &copy; 2015 Dan O'Day

## Future Goals

 - Parse different latitude and longitude formats (currently only accepts signed degrees format).
 - Add option to plot both originating and terminating cell sites / towers (currently you just can run the data through twice, once for originating and again for terminating, being sure to save the files in such a way that the distinction is maintained; Google Earth allows you to view multiple map files simultaneously).
 - Parse date/time fields as date objects to allow for time span slider.
 - Accept data where towers and CDRs span multiple network elements / switches, allowing user to specify which network element names correspond to specific switch names.
 - Visually show azimuth and approximate sector coverage in map file (without committing errors of the 'granularization theory').<sup>1</sup>

----------------------------

<sub><sup>1</sup> Cf. *UNITED STATES V. ANTONIO EVANS*, 892 F. Supp2D. 949 (N.D. ILL. 2012), specifically U.S. District Judge Joan H. Lefkow's opinion and order.</sub>
