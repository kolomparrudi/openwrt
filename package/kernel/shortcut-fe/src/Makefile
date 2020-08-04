#
# Makefile for Shortcut FE.
#

ifeq ($(CONFIG_IPV6),y)
SFE_SUPPORT_IPV6=y
endif
ifeq ($(CONFIG_IPV6),m)
SFE_SUPPORT_IPV6=y
endif

obj-m += shortcut-fe.o shortcut-fe-ipv6.o shortcut-fe-cm.o fast-classifier.o

shortcut-fe-objs := \
    sfe_ipv4.o

shortcut-fe-ipv6-objs := \
    sfe_ipv6.o

shortcut-fe-cm-objs := \
    sfe_cm.o

ccflags-$(SFE_SUPPORT_IPV6) += -DSFE_SUPPORT_IPV6
#-DSFE_TOS
ccflags-y += -DCONFIG_NF_CONNTRACK_CHAIN_EVENTS
