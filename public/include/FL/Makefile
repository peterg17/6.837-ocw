#
# "$Id: Makefile.in,v 1.1.2.9 2004/10/18 20:22:21 easysw Exp $"
#
# Header makefile for the Fast Light Tool Kit (FLTK).
#
# Copyright 1998-2004 by Bill Spitzak and others.
#
# This library is free software; you can redistribute it and/or
# modify it under the terms of the GNU Library General Public
# License as published by the Free Software Foundation; either
# version 2 of the License, or (at your option) any later version.
#
# This library is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
# Library General Public License for more details.
#
# You should have received a copy of the GNU Library General Public
# License along with this library; if not, write to the Free Software
# Foundation, Inc., 59 Temple Place, Suite 330, Boston, MA 02111-1307
# USA.
#
# Please report all bugs and problems to "fltk-bugs@fltk.org".
#

include ../makeinclude

all:

install:
	echo "Installing include files in $(DESTDIR)$(includedir)..."
	-$(MKDIR) -p $(DESTDIR)$(includedir)
	$(RMDIR) $(DESTDIR)$(includedir)/FL
	$(MKDIR) $(DESTDIR)$(includedir)/FL
	$(CHMOD) 755 $(DESTDIR)$(includedir)/FL
	$(CP) ../FL/*.[hHr] $(DESTDIR)$(includedir)/FL
	$(CHMOD) 644 $(DESTDIR)$(includedir)/FL/*.[hHr]
	cd $(DESTDIR)$(includedir)/FL;\
	for file in *.H; do\
		$(RM) "`basename $$file H`h";\
		$(LN) $$file "`basename $$file H`h";\
	done
	$(RM) $(DESTDIR)$(includedir)/FL/fl_file_chooser.H
	$(LN) Fl_File_Chooser.H $(DESTDIR)$(includedir)/FL/fl_file_chooser.H
	$(RM) $(DESTDIR)$(includedir)/FL/fl_file_chooser.h
	$(LN) Fl_File_Chooser.H $(DESTDIR)$(includedir)/FL/fl_file_chooser.h
	$(RM) $(DESTDIR)$(includedir)/Fl
	$(LN) FL $(DESTDIR)$(includedir)/Fl

uninstall:
	echo "Uninstalling include files..."
	$(RMDIR) $(DESTDIR)$(includedir)/FL
	$(RM) $(DESTDIR)$(includedir)/Fl


#
# End of "$Id: Makefile.in,v 1.1.2.9 2004/10/18 20:22:21 easysw Exp $".
#
