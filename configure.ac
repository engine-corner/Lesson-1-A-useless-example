AC_PREREQ([2.69])
AC_INIT([useless-engine], [1.0])
AC_CONFIG_HEADERS([config.h])
AC_CONFIG_MACRO_DIR([m4])

dnl m4_include([m4/ax_check_openssl.m4])

AM_INIT_AUTOMAKE
LT_INIT([disable-static pic-only])

AC_PROG_CC
AC_LANG(C)

AC_CHECK_HEADERS([openssl/engine.h])

AX_CHECK_OPENSSL(
  [have_openssl=yes],
  AC_MSG_FAILURE([could not locate OpenSSL])
)

if test "x$have_openssl" = "xyes"; then
  LIBS="$LIBS $OPENSSL_LIBS"
  CFLAGS="$CFLAGS $OPENSSL_INCLUDES"
  LDFLAGS="$LDFLAGS $OPENSSL_LDFLAGS"
fi

AC_CONFIG_FILES([Makefile])
AC_OUTPUT
