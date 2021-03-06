Net::Bonjour
================
This is a set of perl modules to utilize DNS for service
discovery.  This method of service discovery is branded as Bonjour by 
Apple Computer.  More information can be found at:

http://www.zeroconf.org/
http://developer.apple.com/macosx/bonjour/index.html

A list of register service types can be found at:

http://www.dns-sd.org/ServiceTypes.html

Requirements: 
  perl >= 5.6.0
  Net::DNS >= 0.50

Install the library by running these commands:

   perl Makefile.PL
   make
   make test
   make install

Please report any bugs/suggestions to George Chlipala <george@walnutcs.com>

NOTE FOR Net::Rendezvous USERS

- As with the change by Apple, I have updated the module to use the "Bonjour" name.
  I have added support for the Net::Rendezvous classes as subclasses of the cooresponding
  Net::Bonjour classes.  Although, I would suggest updating scripts to reflect the change.

SPECIAL CHARACTERS IN DNS NAMES

- Previous versions of Net::DNS (0.44) would have issues with special characters in DNS 
  names.  Handling of special characters was added to Net::DNS with version 0.50 rc 1. 
  As of version 0.95, Net::Bonjour::Entry has been updated to recognize the escaped 
  characters and return an interpolated string when the name() method is called.  This
  update was tested against Net::DNS v0.59. If there are any irregularities with a lower
  version, I suggest upgrading Net::DNS to v0.59.

All files contained in this installation are Copyright (c) 2004
George Chlipala unless otherwise specified. All rights reserved.

This library is free software; you can redistribute it and/or modify it under 
the same terms as Perl itself.

Bonjour (in this context) is a trademark of Apple Computer, Inc.
