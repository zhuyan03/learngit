*-D_GNU_SOURCE
**_GNU_SOURCE enables GNU extensions to the C and OS standards supported by the GNU C library, such as asprintf. Define it when you're using such non-standard functions and macros.
**编译avahi-core的时候，一开始总是卡在socket.c，CMAKE_C_FLAGS添加该选项后即可编译通过：
invalid application of 'sizeof' to incomplete type 'struct in6_pktinfo' size_t cmsg_data[(CMSG_SPACE(sizeof(struct in6_pktinfo))/sizeof(size_t)) + 1];
