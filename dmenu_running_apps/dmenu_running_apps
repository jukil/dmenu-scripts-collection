#!/bin/bash
# Search through open programs and switch to their tag
application=$(
	# List all running programs
	xlsclients |\
	# Fix Virtualbox and LibreOffice
   	sed -e 's/.*VirtualBox/foobar  virtualbox/g' -e 's/.*soffice/foobar  libreoffice/g' |\
	# Remove flash from results
	grep -v "plugin-container" |\
	# Show only app-names
   	cut -d" " -f3 |\
	# Pipe to dmenu ($@ to include font settings from dwm/config.h)
	dmenu -i -p "Switch to" $@
)

# Switch to chosen application
case $application in
	gimp | truecrypt)
		xdotool search --onlyvisible -classname "$application" windowactivate &> /dev/null
		;;
	*)
		xdotool search ".*${application}.*" windowactivate &> /dev/null
		;;
esac
