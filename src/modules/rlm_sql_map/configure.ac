#
# Autoconf input file.
#
# Version:	$Id$
#

AC_PREREQ([2.59])
AC_INIT(rlm_sql_map.c)
AC_REVISION($Revision$)
AC_DEFUN(modname,[rlm_sql_map])

AC_ARG_WITH([]modname,
[  --with-[]modname              build []modname. (default=yes)])

if test x$with_[]modname != xno; then

	dnl  This module doesn't need any autoconf test which is not already
	dnl  in top-level configure.

	targetname=modname
else
	targetname=
	echo \*\*\* module modname is disabled.
fi

mod_ldflags="$SMART_LIBS"
mod_cflags="$SMART_CPPFLAGS"
AC_SUBST(mod_ldflags)
AC_SUBST(mod_cflags)
AC_SUBST(targetname)
AC_OUTPUT(all.mk)
