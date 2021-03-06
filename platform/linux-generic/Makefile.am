# Uncomment this if you need to change the CUSTOM_STR string
#export CUSTOM_STR=https://github.com/Linaro/odp.git

include $(top_srcdir)/platform/Makefile.inc

AM_CPPFLAGS =  -I$(srcdir)/include
AM_CPPFLAGS +=  -I$(top_srcdir)/include
AM_CPPFLAGS +=  -I$(top_srcdir)/platform/$(with_platform)/arch
AM_CPPFLAGS +=  -I$(top_srcdir)/include/odp/arch/@ARCH_ABI@
AM_CPPFLAGS +=  -I$(top_builddir)/include
AM_CPPFLAGS +=  -Iinclude
AM_CPPFLAGS +=  -I$(top_srcdir)/platform/$(with_platform)/arch/$(ARCH_DIR)
AM_CPPFLAGS +=  -I$(top_srcdir)/platform/$(with_platform)/arch/default
AM_CPPFLAGS +=  -DSYSCONFDIR=\"@sysconfdir@\"

AM_CPPFLAGS +=  $(OPENSSL_CPPFLAGS)
AM_CPPFLAGS +=  $(DPDK_CPPFLAGS)
AM_CPPFLAGS +=  $(NETMAP_CPPFLAGS)

if PKTIO_DPDK
if ARCH_IS_X86
AM_CFLAGS += -msse4.2
endif
endif

odpincludedir= $(includedir)/odp
odpinclude_HEADERS = \
		  include/odp/visibility_begin.h \
		  include/odp/visibility_end.h

odpapiincludedir= $(includedir)/odp/api
odpapiinclude_HEADERS = \
		  include/odp/api/align.h \
		  include/odp/api/atomic.h \
		  include/odp/api/barrier.h \
		  include/odp/api/buffer.h \
		  include/odp/api/byteorder.h \
		  include/odp/api/chksum.h \
		  include/odp/api/classification.h \
		  include/odp/api/compiler.h \
		  include/odp/api/cpu.h \
		  include/odp/api/cpumask.h \
		  include/odp/api/crypto.h \
		  include/odp/api/debug.h \
		  include/odp/api/deprecated.h \
		  include/odp/api/errno.h \
		  include/odp/api/event.h \
		  include/odp/api/feature.h \
		  include/odp/api/hash.h \
		  include/odp/api/hints.h \
		  include/odp/api/init.h \
		  include/odp/api/ipsec.h \
		  include/odp/api/packet_flags.h \
		  include/odp/api/packet.h \
		  include/odp/api/packet_io.h \
		  include/odp/api/packet_io_stats.h \
		  include/odp/api/pool.h \
		  include/odp/api/queue.h \
		  include/odp/api/random.h \
		  include/odp/api/rwlock.h \
		  include/odp/api/rwlock_recursive.h \
		  include/odp/api/schedule.h \
		  include/odp/api/schedule_types.h \
		  include/odp/api/shared_memory.h \
		  include/odp/api/spinlock.h \
		  include/odp/api/spinlock_recursive.h \
		  include/odp/api/std_clib.h \
		  include/odp/api/std_types.h \
		  include/odp/api/support.h \
		  include/odp/api/sync.h \
		  include/odp/api/system_info.h \
		  include/odp/api/thread.h \
		  include/odp/api/threshold.h \
		  include/odp/api/thrmask.h \
		  include/odp/api/ticketlock.h \
		  include/odp/api/time.h \
		  include/odp/api/timer.h \
		  include/odp/api/traffic_mngr.h \
		  include/odp/api/version.h

odpapiplatincludedir= $(includedir)/odp/api/plat
odpapiplatinclude_HEADERS = \
		  include/odp/api/plat/atomic_inlines.h \
		  include/odp/api/plat/atomic_types.h \
		  include/odp/api/plat/barrier_types.h \
		  include/odp/api/plat/buffer_types.h \
		  include/odp/api/plat/byteorder_inlines.h \
		  include/odp/api/plat/byteorder_types.h \
		  include/odp/api/plat/classification_types.h \
		  include/odp/api/plat/cpumask_types.h \
		  include/odp/api/plat/crypto_types.h \
		  include/odp/api/plat/event_types.h \
		  include/odp/api/plat/init_types.h \
		  include/odp/api/plat/ipsec_types.h \
		  include/odp/api/plat/packet_flag_inlines.h \
		  include/odp/api/plat/packet_flag_inlines_api.h \
		  include/odp/api/plat/packet_inlines.h \
		  include/odp/api/plat/packet_inlines_api.h \
		  include/odp/api/plat/packet_types.h \
		  include/odp/api/plat/packet_io_types.h \
		  include/odp/api/plat/pool_types.h \
		  include/odp/api/plat/queue_types.h \
		  include/odp/api/plat/rwlock_types.h \
		  include/odp/api/plat/rwlock_recursive_types.h \
		  include/odp/api/plat/schedule_types.h \
		  include/odp/api/plat/shared_memory_types.h \
		  include/odp/api/plat/spinlock_types.h \
		  include/odp/api/plat/spinlock_recursive_types.h \
		  include/odp/api/plat/std_clib_inlines.h \
		  include/odp/api/plat/strong_types.h \
		  include/odp/api/plat/sync_inlines.h \
		  include/odp/api/plat/thread_types.h \
		  include/odp/api/plat/thrmask_types.h \
		  include/odp/api/plat/ticketlock_inlines.h \
		  include/odp/api/plat/ticketlock_inlines_api.h \
		  include/odp/api/plat/ticketlock_types.h \
		  include/odp/api/plat/time_types.h \
		  include/odp/api/plat/timer_types.h \
		  include/odp/api/plat/traffic_mngr_types.h \
		  include/odp/api/plat/version_types.h

nodist_odpapiplatinclude_HEADERS = \
		  include/odp/api/plat/static_inline.h

noinst_HEADERS = \
		  arch/odp_arch_time_internal.h \
		  include/_fdserver_internal.h \
		  include/_ishm_internal.h \
		  include/_ishmphy_internal.h \
		  include/_ishmpool_internal.h \
		  include/odp_align_internal.h \
		  include/odp_atomic_internal.h \
		  include/odp_buffer_inlines.h \
		  include/odp_bitmap_internal.h \
		  include/odp_bitset.h \
		  include/odp_buffer_internal.h \
		  include/odp_classification_datamodel.h \
		  include/odp_classification_inlines.h \
		  include/odp_classification_internal.h \
		  include/odp_config_internal.h \
		  include/odp_crypto_internal.h \
		  include/odp_debug_internal.h \
		  include/odp_errno_define.h \
		  include/odp_forward_typedefs_internal.h \
		  include/odp_internal.h \
		  include/odp_ipsec_internal.h \
		  include/odp_llqueue.h \
		  include/odp_name_table_internal.h \
		  include/odp_packet_internal.h \
		  include/odp_packet_io_internal.h \
		  include/odp_packet_io_ipc_internal.h \
		  include/odp_packet_io_ring_internal.h \
		  include/odp_packet_netmap.h \
		  include/odp_packet_dpdk.h \
		  include/odp_packet_socket.h \
		  include/odp_packet_tap.h \
		  include/odp_pkt_queue_internal.h \
		  include/odp_pool_internal.h \
		  include/odp_posix_extensions.h \
		  include/odp_queue_internal.h \
		  include/odp_queue_scalable_internal.h \
		  include/odp_ring_internal.h \
		  include/odp_queue_if.h \
		  include/odp_schedule_if.h \
		  include/odp_schedule_scalable.h \
		  include/odp_schedule_scalable_config.h \
		  include/odp_schedule_scalable_ordered.h \
		  include/odp_sorted_list_internal.h \
		  include/odp_shm_internal.h \
		  include/odp_timer_internal.h \
		  include/odp_timer_wheel_internal.h \
		  include/odp_traffic_mngr_internal.h \
		  include/protocols/eth.h \
		  include/protocols/ip.h \
		  include/protocols/ipsec.h \
		  include/protocols/tcp.h \
		  include/protocols/thash.h \
		  include/protocols/udp.h

__LIB__libodp_linux_la_SOURCES = \
			   _fdserver.c \
			   _ishm.c \
			   _ishmphy.c \
			   _ishmpool.c \
			   odp_atomic.c \
			   odp_barrier.c \
			   odp_bitmap.c \
			   odp_buffer.c \
			   odp_byteorder.c \
			   odp_chksum.c \
			   odp_classification.c \
			   odp_cpu.c \
			   odp_cpumask.c \
			   odp_cpumask_task.c \
			   odp_crypto.c \
			   odp_errno.c \
			   odp_event.c \
			   odp_hash.c \
			   odp_init.c \
			   odp_impl.c \
			   odp_ipsec.c \
			   odp_ipsec_events.c \
			   odp_ipsec_sad.c \
			   odp_name_table.c \
			   odp_packet.c \
			   odp_packet_flags.c \
			   odp_packet_io.c \
			   pktio/ethtool.c \
			   pktio/io_ops.c \
			   pktio/ipc.c \
			   pktio/pktio_common.c \
			   pktio/loop.c \
			   pktio/netmap.c \
			   pktio/dpdk.c \
			   pktio/socket.c \
			   pktio/socket_mmap.c \
			   pktio/sysfs.c \
			   pktio/tap.c \
			   pktio/ring.c \
			   odp_pkt_queue.c \
			   odp_pool.c \
			   odp_queue.c \
			   odp_queue_if.c \
			   odp_queue_scalable.c \
			   odp_rwlock.c \
			   odp_rwlock_recursive.c \
			   odp_schedule.c \
			   odp_schedule_if.c \
			   odp_schedule_sp.c \
			   odp_schedule_iquery.c \
			   odp_schedule_scalable.c \
			   odp_schedule_scalable_ordered.c \
			   odp_shared_memory.c \
			   odp_sorted_list.c \
			   odp_spinlock.c \
			   odp_spinlock_recursive.c \
			   odp_std_clib.c \
			   odp_sync.c \
			   odp_system_info.c \
			   odp_thread.c \
			   odp_thrmask.c \
			   odp_ticketlock.c \
			   odp_time.c \
			   odp_timer.c \
			   odp_timer_wheel.c \
			   odp_traffic_mngr.c \
			   odp_version.c \
			   odp_weak.c

if ARCH_IS_ARM
__LIB__libodp_linux_la_SOURCES += arch/default/odp_cpu_cycles.c \
				  arch/default/odp_global_time.c \
				  arch/default/odp_sysinfo_parse.c
arch_odp_headers = arch/arm/odp/api/cpu_arch.h
noinst_HEADERS += arch/arm/odp_atomic.h \
		  arch/arm/odp_cpu.h \
		  arch/arm/odp_cpu_idling.h \
		  arch/default/odp_cpu_idling.h \
		  arch/arm/odp_llsc.h
endif
if ARCH_IS_AARCH64
__LIB__libodp_linux_la_SOURCES += arch/default/odp_cpu_cycles.c \
				  arch/aarch64/odp_global_time.c \
				  arch/default/odp_sysinfo_parse.c
arch_odp_headers = arch/aarch64/odp/api/cpu_arch.h
noinst_HEADERS += arch/aarch64/odp_atomic.h \
		  arch/aarch64/odp_cpu.h \
		  arch/aarch64/odp_cpu_idling.h \
		  arch/default/odp_cpu_idling.h \
		  arch/aarch64/odp_llsc.h
endif
if ARCH_IS_MIPS64
__LIB__libodp_linux_la_SOURCES += arch/mips64/odp_cpu_cycles.c \
				  arch/default/odp_global_time.c \
				  arch/mips64/odp_sysinfo_parse.c
arch_odp_headers = arch/mips64/odp/api/cpu_arch.h
noinst_HEADERS += arch/default/odp_cpu.h \
		  arch/default/odp_cpu_idling.h
endif
if ARCH_IS_POWERPC
__LIB__libodp_linux_la_SOURCES += arch/default/odp_cpu_cycles.c \
				  arch/default/odp_global_time.c \
				  arch/powerpc/odp_sysinfo_parse.c
arch_odp_headers = arch/powerpc/odp/api/cpu_arch.h
noinst_HEADERS += arch/default/odp_cpu.h \
		  arch/default/odp_cpu_idling.h
endif
if ARCH_IS_X86
__LIB__libodp_linux_la_SOURCES += arch/x86/cpu_flags.c \
				  arch/x86/odp_cpu_cycles.c \
				  arch/x86/odp_global_time.c \
				  arch/x86/odp_sysinfo_parse.c
arch_odp_headers = arch/x86/odp/api/cpu_arch.h
noinst_HEADERS += arch/x86/cpu_flags.h
noinst_HEADERS += arch/default/odp_cpu.h \
		  arch/default/odp_cpu_idling.h
endif

noinst_HEADERS += arch/default/odp/api/cpu_arch.h

odpapiinclude_HEADERS += $(arch_odp_headers)

if HAVE_PCAP
__LIB__libodp_linux_la_SOURCES += pktio/pcap.c
endif

__LIB__libodp_linux_la_LIBADD = $(ATOMIC_LIBS)
__LIB__libodp_linux_la_LIBADD += $(OPENSSL_LIBS)
__LIB__libodp_linux_la_LIBADD += $(DPDK_LIBS) $(DPDK_PMDS)
__LIB__libodp_linux_la_LIBADD += $(PTHREAD_LIBS)
__LIB__libodp_linux_la_LIBADD += $(TIMER_LIBS)

if HAVE_PCAP
__LIB__libodp_linux_la_LIBADD += $(PCAP_LIBS)
endif
