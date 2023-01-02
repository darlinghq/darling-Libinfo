project(libinfo-rpc)

include_directories(${CMAKE_CURRENT_SOURCE_DIR})

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -fblocks")

set(info-rpc_sources
	auth_none.c
	auth_unix.c
	authunix_prot.c
	bindresvport.c
	clnt_generic.c
	clnt_perror.c
	clnt_raw.c
	clnt_simple.c
	clnt_tcp.c
	clnt_udp.c
	get_myaddress.c
	getrpcent.c
	getrpcport.c
	pmap_clnt.c
	pmap_getmaps.c
	pmap_getport.c
	pmap_prot.c
	pmap_prot2.c
	pmap_rmt.c
	pmap_wakeup.c
	rpc_callmsg.c
	rpc_commondata.c
	rpc_dtablesize.c
	rpc_prot.c
	svc.c
	svc_auth.c
	svc_auth_unix.c
	svc_raw.c
	svc_run.c
	svc_simple.c
	svc_tcp.c
	svc_udp.c
	xdr.c
	xdr_array.c
	xdr_float.c
	xdr_mem.c
	xdr_rec.c
	xdr_reference.c
	xdr_sizeof.c
	xdr_stdio.c
)

add_darling_object_library(info-rpc ${info-rpc_sources})
