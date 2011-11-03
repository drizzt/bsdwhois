#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_INIT([bsdwhois], [1.50])
AM_CONFIG_HEADER([src/config.h])
AM_INIT_AUTOMAKE

# Checks for programs.
AC_PROG_CC

# Checks for libraries.

# Checks for header files.
AC_HEADER_STDC
AC_CHECK_HEADERS([arpa/inet.h netdb.h netinet/in.h stdlib.h string.h sys/socket.h unistd.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_C_CONST
AC_TYPE_SIZE_T
AC_TYPE_SSIZE_T

# Checks for library functions.
AC_CHECK_FUNCS([memset socket strcasecmp strchr])
AC_CHECK_FUNCS([fgetln strnstr])

AM_CONDITIONAL(NEED_FGETLN, test x"$ac_cv_func_fgetln" = xno)
AM_CONDITIONAL(NEED_STRNSTR, test x"$ac_cv_func_strnstr" = xno)

AH_BOTTOM([
#ifndef HAVE_FGETLN
extern char *fgetln(FILE *stream, size_t *len);
#endif
#ifndef HAVE_STRNSTR
extern char *strnstr(const char *big, const char *little, size_t len);
#endif
])

AC_OUTPUT([Makefile src/Makefile])
