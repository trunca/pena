installdir = $(pkglibdir)/python/Plugins/SystemPlugins

SUBDIRS = SoftwareManager PositionerSetup Satfinder \
	SkinSelector SatelliteEquipmentControl Videomode VideoTune Hotplug \
	DefaultServicesScanner DiseqcTester CommonInterfaceAssignment GBAspectRatioSwitch \
	CableScan FastScan OSDPositionSetup OSD3DSetup HdmiCEC VideoClippingSetup \
	VideoEnhancement WirelessLan NetworkWizard DeviceManager \
	SwapManager SoftcamStartup

if HAVE_OSDANIMATION
SUBDIRS += AnimationSetup
endif

if GB7252
SUBDIRS += QuadPiP
endif

install_PYTHON =	\
	__init__.py
