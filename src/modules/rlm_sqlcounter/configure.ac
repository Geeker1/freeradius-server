AC_PREREQ([2.53])
AC_INIT(rlm_sqlcounter.c)
AC_REVISION($Revision$)
AC_DEFUN(modname,[rlm_sqlcounter])

AC_ARG_WITH([]modname,
[  --with-[]modname              build []modname. (default=yes)])

if test x$with_[]modname != xno; then

	AC_PROG_CC
	AC_PROG_CPP

	targetname=modname
else
	targetname=
	echo \*\*\* module modname is disabled.
fi

if test x"$fail" != x""; then
	if test x"${enable_strict_dependencies}" = x"yes"; then
		AC_MSG_ERROR([set --without-]modname[ to disable it explicitly.])
	else
		AC_MSG_WARN([silently not building ]modname[.])
		AC_MSG_WARN([FAILURE: ]modname[ requires: $fail.]);
		targetname=""
	fi
fi

mod_ldflags="$SMART_LIBS"
mod_cflags="$SMART_CPPFLAGS"
AC_SUBST(mod_ldflags)
AC_SUBST(mod_cflags)
AC_SUBST(targetname)
AC_OUTPUT(all.mk)
