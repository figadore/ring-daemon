include $(top_srcdir)/globals.mk

SUBDIRS = eth/libdevcore eth/libdevcrypto

AM_CPPFLAGS += -I$(top_srcdir)/src/jamidht/eth
noinst_LTLIBRARIES = libringacc.la

libringacc_la_CXXFLAGS = @CXXFLAGS@ @JSONCPP_CFLAGS@

libringacc_la_LIBADD = $(DHT_LIBS) \
    ./eth/libdevcore/libdevcore.la \
    ./eth/libdevcrypto/libdevcrypto.la

libringacc_la_SOURCES = \
        abstract_sip_transport.h \
        jamiaccount.cpp \
        jamiaccount.h \
        connectionmanager.h \
        connectionmanager.cpp \
        channeled_transport.h \
        channeled_transport.cpp \
        channeled_transfers.h \
        channeled_transfers.cpp \
        multiplexed_socket.h \
        multiplexed_socket.cpp \
        sips_transport_ice.cpp \
        sips_transport_ice.h \
        accountarchive.cpp \
        accountarchive.h \
        p2p.cpp \
        p2p.h \
        contact_list.h \
        contact_list.cpp \
        account_manager.h \
        account_manager.cpp \
        archive_account_manager.h \
        archive_account_manager.cpp \
        server_account_manager.h \
        server_account_manager.cpp

if RINGNS
libringacc_la_SOURCES += \
        namedirectory.cpp \
        namedirectory.h
endif

nobase_include_HEADERS= jami_contact.h
