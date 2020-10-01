
obj-m	+= bcachefs.o

bcachefs-y		:=	\
	acl.o			\
	alloc_background.o	\
	alloc_foreground.o	\
	bkey.o			\
	bkey_methods.o		\
	bkey_sort.o		\
	bset.o			\
	btree_cache.o		\
	btree_gc.o		\
	btree_io.o		\
	btree_iter.o		\
	btree_key_cache.o	\
	btree_update_interior.o	\
	btree_update_leaf.o	\
	buckets.o		\
	chardev.o		\
	checksum.o		\
	clock.o			\
	compress.o		\
	debug.o			\
	dirent.o		\
	disk_groups.o		\
	ec.o			\
	error.o			\
	extents.o		\
	extent_update.o		\
	fs.o			\
	fs-common.o		\
	fs-ioctl.o		\
	fs-io.o			\
	fsck.o			\
	inode.o			\
	io.o			\
	journal.o		\
	journal_io.o		\
	journal_reclaim.o	\
	journal_seq_blacklist.o	\
	keylist.o		\
	migrate.o		\
	move.o			\
	movinggc.o		\
	opts.o			\
	quota.o			\
	rebalance.o		\
	recovery.o		\
	reflink.o		\
	replicas.o		\
	siphash.o		\
	super.o			\
	super-io.o		\
	sysfs.o			\
	tests.o			\
	trace.o			\
	util.o			\
	xattr.o

all:
	cp ../../include/linux/closure.h /lib/modules/$(shell uname -r)/build/include/linux
	cp ../../include/linux/six.h /lib/modules/$(shell uname -r)/build/include/linux
	cp ../../include/trace/events/bcachefs.h /lib/modules/$(shell uname -r)/build/include/trace/events
	$(MAKE) -C /lib/modules/$(shell uname -r)/build M=$$PWD modules

clean:
	$(MAKE) -C /lib/modules/$(shell uname -r)/build M=$$PWD clean modules
