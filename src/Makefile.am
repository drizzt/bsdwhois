AUTOMAKE_OPTIONS = foreign

bin_PROGRAMS = whois
whois_SOURCES = whois.c
man_MANS= whois.1

if NEED_FGETLN
whois_SOURCES += fgetln.c
endif
if NEED_STRNSTR
whois_SOURCES += strnstr.c
endif

EXTRA_DIST = $(man_MANS)
