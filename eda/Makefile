.SILENT:
.PHONY: all cmd clean realclean distclean

# CROSS-PLATFORM MAGIC

include ../include.mk

all:
	@$(call echo,Building Ecere Data Access layer...)
	cd libeda && $(MAKE)
	@$(call echo,Building EDASQLite driver...)
	cd drivers && cd sqlite && $(MAKE)
ifdef EDASQLiteCipher
	@$(call echo,Building EDASQLiteCipher driver...)
	cd drivers && cd sqliteCipher && $(MAKE)
endif

clean:
	cd libeda && $(MAKE) clean
	cd drivers && cd sqlite && $(MAKE) clean
ifdef EDASQLiteCipher
	cd drivers && cd sqliteCipher && $(MAKE) clean
endif

realclean:
	cd libeda && $(MAKE) realclean
	cd drivers && cd sqlite && $(MAKE) realclean
ifdef EDASQLiteCipher
	cd drivers && cd sqliteCipher && $(MAKE) realclean
endif

distclean:
	cd libeda && $(MAKE) distclean
	cd drivers && cd sqlite && $(MAKE) distclean
ifdef EDASQLiteCipher
	cd drivers && cd sqliteCipher && $(MAKE) distclean
endif
