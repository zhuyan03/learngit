# <center>-D_GNU_SOURCE</center><br>
## _GNU_SOURCE enables GNU extensions to the C and OS standards supported by the GNU C library, such as asprintf.<br>
Define it when you're using such non-standard functions and macros.
## 编译avahi-core的时候，一开始总是卡在socket.c，CMAKE_C_FLAGS添加该选项后即可编译通过：
invalid application of 'sizeof' to incomplete type 'struct in6_pktinfo' size_t cmsg_data[(CMSG_SPACE(sizeof(struct in6_pktinfo))/sizeof(size_t)) + 1];
## [From glibc manual](http://www.gnu.org/software/libc/manual/html_node/Feature-Test-Macros.html):
Macro: _GNU_SOURCE
If you define this macro, everything is included: ISO C89, ISO C99, POSIX.1, POSIX.2, BSD, SVID, X/Open, LFS, and GNU extensions. In the cases where POSIX.1 conflicts with BSD, the POSIX definitions take precedence.

## refrence:[What does “#define _GNU_SOURCE” imply](https://stackoverflow.com/questions/5582211/what-does-define-gnu-source-imply)
