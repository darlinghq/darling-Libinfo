project(libinfo-nis)

cmake_minimum_required(VERSION 3.13)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../../libc/locale)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../../libc/locale/FreeBSD)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../../libc/pthreads)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../../libc/stdtime/FreeBSD)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../../external/libdispatch/)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../../external/libdispatch/private)
include_directories(${CMAKE_CURRENT_SOURCE_DIR})

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -fblocks")

set(info-nis_sources
	getdomainname.c
	innetgr.c
	setdomainname.c
	xdr_domainname.c
	xdr_keydat.c
	xdr_mapname.c
	xdr_peername.c
	xdr_valdat.c
	xdr_ypbind_binding.c
	xdr_ypbind_resp.c
	xdr_ypbind_resptype.c
	xdr_ypbind_setdom.c
	xdr_ypmaplist.c
	xdr_ypreq_key.c
	xdr_ypreq_nokey.c
	xdr_ypresp_all.c
	xdr_ypresp_key_val.c
	xdr_ypresp_maplist.c
	xdr_ypresp_master.c
	xdr_ypresp_order.c
	xdr_ypresp_val.c
	xdr_ypstat.c
	yp_all.c
	yp_bind.c
	yp_first.c
	yp_get_default_domain.c
	yp_maplist.c
	yp_master.c
	yp_order.c
	yperr_string.c
	ypmatch_cache.c
	yppasswdd_xdr.c
	ypprot_err.c
)

add_darling_object_library(info-nis ${info-nis_sources})
