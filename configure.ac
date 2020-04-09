AC_INIT(check_ssh_key, VERSION_DEV, lars@oddbit.com)

AC_CHECK_LIB(ssh2,libssh2_init,,[AC_MSG_ERROR([libssh2 not found.])])

FOUND_SSL_LIB="no"
AC_CHECK_LIB(ssl, OPENSSL_init_ssl, [FOUND_SSL_LIB="yes"])
AC_CHECK_LIB(ssl, SSL_library_init, [FOUND_SSL_LIB="yes"])
AS_IF([test "x$FOUND_SSL_LIB" = xno], [AC_MSG_ERROR([libssl not found])])

AC_CONFIG_FILES([Makefile])
AC_OUTPUT

