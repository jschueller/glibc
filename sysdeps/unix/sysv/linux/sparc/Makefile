abi-variants := 32 64
abi-32-condition := __WORDSIZE == 32
abi-64-condition := __WORDSIZE == 64

ifeq ($(subdir),rt)
librt-routines += rt-sysdep
librt-shared-only-routines += rt-sysdep
endif

ifeq ($(subdir),sysvipc)
sysdep_routines += getshmlba
endif

ifeq ($(subdir),signal)
sysdep_routines += sigreturn_stub
endif

ifeq ($(subdir),nptl)
# pull in __syscall_error routine
libpthread-routines += sysdep sigreturn_stub
libpthread-shared-only-routines += sysdep sigreturn_stub
endif
