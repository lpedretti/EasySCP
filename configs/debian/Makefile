#!/usr/bin/make -f

# EasySCP a Virtual Hosting Control Panel
# Copyright (C) 2010-2018 by Easy Server Control Panel - http://www.easyscp.net
#
# This work is licensed under the Creative Commons Attribution-NoDerivs 3.0 Unported License.
# To view a copy of this license, visit http://creativecommons.org/licenses/by-nd/3.0/.
#
# @link 		http://www.easyscp.net
# @author 		EasySCP Team

export

OS := $(shell lsb_release -sc)

install:
		cd ./apache && $(MAKE) install
		cd ./init.d && $(MAKE) install
		cd ./systemd && $(MAKE) install
		cp -pR ./tpl $(SYSTEM_CONF)
		cp -p ./EasySCP_CMD_$(OS).xml $(SYSTEM_CONF)/EasySCP_CMD.xml
		cp -p ./EasySCP_Distro_$(OS).xml $(SYSTEM_CONF)/EasySCP_Distro.xml

uninstall:
		cd ./apache && $(MAKE) uninstall
		cd ./init.d && $(MAKE) uninstall
		cd ./systemd && $(MAKE) uninstall
		rm -rf $(SYSTEM_CONF)/tpl
		rm -rf $(SYSTEM_CONF)/easyscp.conf
		rm -rf $(SYSTEM_CONF)/EasySCP_CMD.xml
		rm -rf $(SYSTEM_CONF)/EasySCP_Config.xml
		rm -rf $(SYSTEM_CONF)/EasySCP_Config_DB.php
		rm -rf $(SYSTEM_CONF)/EasySCP_Distro.xml

