SWIG_SOURCES = ../swsscommon.i

pkgpython3_PYTHON = swsscommon.py __init__.py
pkgpy3exec_LTLIBRARIES = _swsscommon.la

_swsscommon_la_SOURCES = swsscommon_wrap.cpp
_swsscommon_la_CPPFLAGS = -std=c++11 -I../../common -I/usr/include/python$(PYTHON3_VERSION)
_swsscommon_la_LDFLAGS = -module
_swsscommon_la_LIBADD = ../../common/libswsscommon.la $(PYTHON3_BLDLIBRARY)

swsscommon_wrap.cpp: $(SWIG_SOURCES)
	$(SWIG) -Wall -c++ -python -keyword -I../../common -o $@ $<

CLEANFILES = swsscommon_wrap.cpp
