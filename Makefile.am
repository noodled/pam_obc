UTOMAKE_OPIONS=foreign no-dependencies
SUBDIRS = src

INCLUDES = @INCLUDES@

# Install BFD include file, and others that it needs.
#install-data-local: 
#       @$(NORMAL_INSTALL)
#       $(mkinstalldirs) $(sysconfdir)
#       $(INSTALL_DATA)sagan.conf $(sysconfdir)/sagan.conf

install-data-local:

#	$(INSTALL) -m 644 src/pam_obc /lib/security/pam_obc.so
	test -e /etc/pam_obc.conf || $(INSTALL) -m 600 etc/pam_obc.conf /etc/pam_obc.conf

	@echo "--------------------------------------------------------------------------------"
	@echo "    * README * README * README * README * README * README * README * README *"
	@echo "--------------------------------------------------------------------------------"
	@echo ""
	@echo "Installation Notes:"
	@echo ""
	@echo "You'll need to copy the pam_obc.so to the correct shared library location."
	@echo "For example:"
	@echo ""
	@echo "cp src/pam_obc /lib/x86_64-linux-gnu/security/pam_obc.so"
	@echo ""
	@echo "Common PAM shared library locations:"
	@echo ""
	@echo "Gentoo: /lib/security"
	@echo "Ubuntu 64 bit: /lib/x86_64-linux-gnu/security/"
	@echo "Ubuntu 32 bit: /lib/security"
	@echo ""
	@echo "You'll then want to add pam_obc.so to any /etc/pam.d configuration files you"
	@echo "want to use it in.  You'd add something like this:"
	@echo ""
	@echo "auth       required    pam_obc.so"
	@echo ""
	@echo "Finally,  edit the /etc/pam_obc.conf.  "
	@echo ""
	@echo "If you're looking to use pam_obc with sshd, make sure that in your sshd_conf"
	@echo "has this line: \"ChallengeResponseAuthentication yes\""
	@echo ""
	@echo "For more information on configuration,  please see the README file or"
	@echo "https://github.com/beave/pam_obc/blob/master/README.md"
	@echo "--------------------------------------------------------------------------------"

