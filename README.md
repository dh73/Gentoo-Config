# Gentoo Linux Configuration
This is my Gentoo configuration files for the **tau** server, which have the following hardware:

*Yeah, I have two RAM memories of different frequencies, due an issue with Amazon which sent erroneous product. Tried refund but RAM was expensive/neccesary that time*.

```bash
tau
    description: Desktop Computer
    product: System Product Name (SKU)
    vendor: System manufacturer
    version: System Version
    serial: System Serial Number
    width: 4294967295 bits
    capabilities: smbios-3.0 dmi-3.0 smp vsyscall32
    configuration: boot=normal chassis=desktop family=To be filled by O.E.M. sku=SKU uuid=E08DF7CA-CAF8-E611-9B18-6045CB9A4B86
  *-core
       description: Motherboard
       product: PRIME X370-PRO
       vendor: ASUSTeK COMPUTER INC.
       physical id: 0
       version: Rev X.0x
       serial: 170295422500914
       slot: Default string
     *-firmware
          description: BIOS
          vendor: American Megatrends Inc.
          physical id: 0
          version: 0502
          date: 02/17/2017
          size: 64KiB
          capacity: 15MiB
          capabilities: pci apm upgrade shadowing cdboot bootselect socketedrom edd int13floppy1200 int13floppy720 int13floppy2880 int5printscreen int9keyboard int14serial int17printer acpi usb biosbootspecification uefi
     *-memory
          description: System Memory
          physical id: 32
          slot: System board or motherboard
          size: 32GiB
        *-bank:0
             description: [empty]
             product: Unknown
             vendor: Unknown
             physical id: 0
             serial: Unknown
             slot: DIMM_A1
        *-bank:1
             description: DIMM DDR4 Synchronous Unbuffered (Unregistered) 2133 MHz (0.5 ns)
             product: KHX2133C
             vendor: Kingston
             physical id: 1
             serial: 4E2A0A3C
             slot: DIMM_A2
             size: 16GiB
             width: 64 bits
             clock: 2133MHz (0.5ns)
        *-bank:2
             description: [empty]
             product: Unknown
             vendor: Unknown
             physical id: 2
             serial: Unknown
             slot: DIMM_B1
        *-bank:3
             description: DIMM DDR4 Synchronous Unbuffered (Unregistered) 2400 MHz (0.4 ns)
             product: KHX2400C
             vendor: Kingston
             physical id: 3
             serial: 92379171
             slot: DIMM_B2
             size: 16GiB
             width: 64 bits
             clock: 2400MHz (0.4ns)
     *-cache:0
          description: L1 cache
          physical id: 34
          slot: L1 - Cache
          size: 768KiB
          capacity: 768KiB
          clock: 1GHz (1.0ns)
          capabilities: pipeline-burst internal write-back unified
          configuration: level=1
     *-cache:1
          description: L2 cache
          physical id: 35
          slot: L2 - Cache
          size: 4MiB
          capacity: 4MiB
          clock: 1GHz (1.0ns)
          capabilities: pipeline-burst internal write-back unified
          configuration: level=2
     *-cache:2
          description: L3 cache
          physical id: 36
          slot: L3 - Cache
          size: 16MiB
          capacity: 16MiB
          clock: 1GHz (1.0ns)
          capabilities: pipeline-burst internal write-back unified
          configuration: level=3
     *-cpu
          description: CPU
          product: AMD Ryzen 7 1700X Eight-Core Processor
          vendor: Advanced Micro Devices [AMD]
          physical id: 37
          bus info: cpu@0
          version: AMD Ryzen 7 1700X Eight-Core Processor
          serial: Unknown
          slot: AM4
          size: 3521MHz
          capacity: 3700MHz
          width: 64 bits
          clock: 100MHz
          capabilities: x86-64 fpu fpu_exception wp vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp constant_tsc rep_good nopl nonstop_tsc cpuid extd_apicid aperfmperf pni pclmulqdq monitor ssse3 fma cx16 sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand lahf_lm cmp_legacy svm extapic cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw skinit wdt tce topoext perfctr_core perfctr_nb bpext perfctr_llc mwaitx cpb hw_pstate sme ssbd sev vmmcall fsgsbase bmi1 avx2 smep bmi2 rdseed adx smap clflushopt sha_ni xsaveopt xsavec xgetbv1 xsaves clzero irperf xsaveerptr arat npt lbrv svm_lock nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold avic v_vmsave_vmload vgif overflow_recov succor smca cpufreq
          configuration: cores=8 enabledcores=8 threads=16
     *-pci:0
          description: Host bridge
          product: Family 17h (Models 00h-0fh) Root Complex
          vendor: Advanced Micro Devices, Inc. [AMD]
          physical id: 100
          bus info: pci@0000:00:00.0
          version: 00
          width: 32 bits
          clock: 33MHz
        *-pci:0
             description: PCI bridge
             product: Family 17h (Models 00h-0fh) PCIe GPP Bridge
             vendor: Advanced Micro Devices, Inc. [AMD]
             physical id: 1.3
             bus info: pci@0000:00:01.3
             version: 00
             width: 32 bits
             clock: 33MHz
             capabilities: pci pm pciexpress msi ht normal_decode bus_master cap_list
             configuration: driver=pcieport
             resources: irq:0 ioport:e000(size=4096) memory:fe500000-fe7fffff ioport:f0200000(size=6291456)
           *-usb
                description: USB controller
                product: Advanced Micro Devices, Inc. [AMD]
                vendor: Advanced Micro Devices, Inc. [AMD]
                physical id: 0
                bus info: pci@0000:03:00.0
                version: 02
                width: 64 bits
                clock: 33MHz
                capabilities: msi pm pciexpress xhci bus_master cap_list
                configuration: driver=xhci_hcd latency=0
                resources: irq:45 memory:fe7a0000-fe7a7fff
              *-usbhost:0
                   product: xHCI Host Controller
                   vendor: Linux 4.19.44-gentoo xhci-hcd
                   physical id: 0
                   bus info: usb@1
                   logical name: usb1
                   version: 4.19
                   capabilities: usb-2.00
                   configuration: driver=hub slots=14 speed=480Mbit/s
                 *-usb
                      description: Mouse
                      product: USB Optical Mouse
                      vendor: Sunplus Innovation Technology Inc.
                      physical id: 5
                      bus info: usb@1:5
                      version: 0.90
                      capabilities: usb-2.00
                      configuration: driver=usbhid maxpower=98mA speed=2Mbit/s
              *-usbhost:1
                   product: xHCI Host Controller
                   vendor: Linux 4.19.44-gentoo xhci-hcd
                   physical id: 1
                   bus info: usb@2
                   logical name: usb2
                   version: 4.19
                   capabilities: usb-3.10
                   configuration: driver=hub slots=8 speed=10000Mbit/s
           *-storage
                description: SATA controller
                product: Advanced Micro Devices, Inc. [AMD]
                vendor: Advanced Micro Devices, Inc. [AMD]
                physical id: 0.1
                bus info: pci@0000:03:00.1
                version: 02
                width: 32 bits
                clock: 33MHz
                capabilities: storage msi pm pciexpress ahci_1.0 bus_master cap_list rom
                configuration: driver=ahci latency=0
                resources: irq:37 memory:fe780000-fe79ffff memory:fe700000-fe77ffff
           *-pci
                description: PCI bridge
                product: Advanced Micro Devices, Inc. [AMD]
                vendor: Advanced Micro Devices, Inc. [AMD]
                physical id: 0.2
                bus info: pci@0000:03:00.2
                version: 02
                width: 32 bits
                clock: 33MHz
                capabilities: pci msi pm pciexpress normal_decode bus_master cap_list
                configuration: driver=pcieport
                resources: irq:28 ioport:e000(size=4096) memory:fe500000-fe6fffff ioport:f0200000(size=6291456)
              *-pci:0
                   description: PCI bridge
                   product: 300 Series Chipset PCIe Port
                   vendor: Advanced Micro Devices, Inc. [AMD]
                   physical id: 0
                   bus info: pci@0000:1d:00.0
                   version: 02
                   width: 32 bits
                   clock: 33MHz
                   capabilities: pci msi pm pciexpress normal_decode bus_master cap_list
                   configuration: driver=pcieport
                   resources: irq:29
              *-pci:1
                   description: PCI bridge
                   product: 300 Series Chipset PCIe Port
                   vendor: Advanced Micro Devices, Inc. [AMD]
                   physical id: 2
                   bus info: pci@0000:1d:02.0
                   version: 02
                   width: 32 bits
                   clock: 33MHz
                   capabilities: pci msi pm pciexpress normal_decode bus_master cap_list
                   configuration: driver=pcieport
                   resources: irq:30 ioport:f0200000(size=2097152)
              *-pci:2
                   description: PCI bridge
                   product: 300 Series Chipset PCIe Port
                   vendor: Advanced Micro Devices, Inc. [AMD]
                   physical id: 3
                   bus info: pci@0000:1d:03.0
                   version: 02
                   width: 32 bits
                   clock: 33MHz
                   capabilities: pci msi pm pciexpress normal_decode bus_master cap_list
                   configuration: driver=pcieport
                   resources: irq:32
              *-pci:3
                   description: PCI bridge
                   product: 300 Series Chipset PCIe Port
                   vendor: Advanced Micro Devices, Inc. [AMD]
                   physical id: 4
                   bus info: pci@0000:1d:04.0
                   version: 02
                   width: 32 bits
                   clock: 33MHz
                   capabilities: pci msi pm pciexpress normal_decode bus_master cap_list
                   configuration: driver=pcieport
                   resources: irq:33 memory:fe600000-fe6fffff
                 *-usb
                      description: USB controller
                      product: ASM1143 USB 3.1 Host Controller
                      vendor: ASMedia Technology Inc.
                      physical id: 0
                      bus info: pci@0000:25:00.0
                      version: 00
                      width: 64 bits
                      clock: 33MHz
                      capabilities: msi pm pciexpress xhci bus_master cap_list
                      configuration: driver=xhci_hcd latency=0
                      resources: irq:46 memory:fe600000-fe607fff
                    *-usbhost:0
                         product: xHCI Host Controller
                         vendor: Linux 4.19.44-gentoo xhci-hcd
                         physical id: 0
                         bus info: usb@3
                         logical name: usb3
                         version: 4.19
                         capabilities: usb-2.00
                         configuration: driver=hub slots=2 speed=480Mbit/s
                       *-usb
                            description: USB hub
                            product: USB2.0 Hub
                            vendor: GenesysLogic
                            physical id: 2
                            bus info: usb@3:2
                            version: 92.24
                            capabilities: usb-2.10
                            configuration: driver=hub maxpower=100mA slots=4 speed=480Mbit/s
                          *-usb:0
                               description: Generic USB device
                               product: USB-Blaster
                               vendor: Altera
                               physical id: 3
                               bus info: usb@3:2.3
                               version: 4.00
                               serial: 91d28408
                               capabilities: usb-1.10
                               configuration: driver=usbfs maxpower=150mA speed=12Mbit/s
                          *-usb:1
                               description: USB hub
                               product: USB2.0 Hub
                               vendor: GenesysLogic
                               physical id: 4
                               bus info: usb@3:2.4
                               version: 92.24
                               capabilities: usb-2.10
                               configuration: driver=hub maxpower=100mA slots=4 speed=480Mbit/s
                    *-usbhost:1
                         product: xHCI Host Controller
                         vendor: Linux 4.19.44-gentoo xhci-hcd
                         physical id: 1
                         bus info: usb@4
                         logical name: usb4
                         version: 4.19
                         capabilities: usb-3.10
                         configuration: driver=hub slots=2 speed=10000Mbit/s
                       *-usb
                            description: USB hub
                            product: USB3.0 Hub
                            vendor: GenesysLogic
                            physical id: 2
                            bus info: usb@4:2
                            version: 92.24
                            capabilities: usb-3.00
                            configuration: driver=hub slots=4 speed=5000Mbit/s
                          *-usb
                               description: USB hub
                               product: USB3.0 Hub
                               vendor: GenesysLogic
                               physical id: 4
                               bus info: usb@4:2.4
                               version: 92.24
                               capabilities: usb-3.00
                               configuration: driver=hub slots=4 speed=5000Mbit/s
                             *-usb
                                  description: Mass storage device
                                  product: USB3.0 Card Reader
                                  vendor: Generic
                                  physical id: 4
                                  bus info: usb@4:2.4.4
                                  logical name: scsi9
                                  version: 15.35
                                  serial: 000000001536
                                  capabilities: usb-3.10 scsi emulated scsi-host
                                  configuration: driver=usb-storage maxpower=896mA speed=5000Mbit/s
                                *-disk:0
                                     description: SCSI Disk
                                     product: MassStorageClass
                                     vendor: Generic
                                     physical id: 0.0.0
                                     bus info: scsi@9:0.0.0
                                     logical name: /dev/sdc
                                     version: 1536
                                     serial: 000000001536
                                     capabilities: removable
                                     configuration: ansiversion=6 logicalsectorsize=512 sectorsize=512
                                   *-medium
                                        physical id: 0
                                        logical name: /dev/sdc
                                *-disk:1
                                     description: SCSI Disk
                                     product: MassStorageClass
                                     vendor: Generic
                                     physical id: 0.0.1
                                     bus info: scsi@9:0.0.1
                                     logical name: /dev/sdd
                                     version: 1536
                                     serial: 000000001536
                                     capabilities: removable
                                     configuration: ansiversion=6 logicalsectorsize=512 sectorsize=512
                                   *-medium
                                        physical id: 0
                                        logical name: /dev/sdd
              *-pci:4
                   description: PCI bridge
                   product: 300 Series Chipset PCIe Port
                   vendor: Advanced Micro Devices, Inc. [AMD]
                   physical id: 6
                   bus info: pci@0000:1d:06.0
                   version: 02
                   width: 32 bits
                   clock: 33MHz
                   capabilities: pci msi pm pciexpress normal_decode bus_master cap_list
                   configuration: driver=pcieport
                   resources: irq:34 ioport:e000(size=4096) memory:fe500000-fe5fffff ioport:f0400000(size=2097152)
                 *-network
                      description: Ethernet interface
                      product: I211 Gigabit Network Connection
                      vendor: Intel Corporation
                      physical id: 0
                      bus info: pci@0000:26:00.0
                      logical name: eth0
                      version: 03
                      serial: 60:45:cb:9a:4b:86
                      size: 1Gbit/s
                      capacity: 1Gbit/s
                      width: 32 bits
                      clock: 33MHz
                      capabilities: pm msi msix pciexpress bus_master cap_list ethernet physical tp 10bt 10bt-fd 100bt 100bt-fd 1000bt-fd autonegotiation
                      configuration: autonegotiation=on broadcast=yes driver=igb driverversion=5.4.0-k duplex=full firmware=0. 6-1 ip=192.168.1.195 latency=0 link=yes multicast=yes port=twisted pair speed=1Gbit/s
                      resources: irq:24 memory:fe500000-fe51ffff ioport:e000(size=32) memory:fe520000-fe523fff
              *-pci:5
                   description: PCI bridge
                   product: 300 Series Chipset PCIe Port
                   vendor: Advanced Micro Devices, Inc. [AMD]
                   physical id: 7
                   bus info: pci@0000:1d:07.0
                   version: 02
                   width: 32 bits
                   clock: 33MHz
                   capabilities: pci msi pm pciexpress normal_decode bus_master cap_list
                   configuration: driver=pcieport
                   resources: irq:35
        *-pci:1
             description: PCI bridge
             product: Family 17h (Models 00h-0fh) PCIe GPP Bridge
             vendor: Advanced Micro Devices, Inc. [AMD]
             physical id: 3.2
             bus info: pci@0000:00:03.2
             version: 00
             width: 32 bits
             clock: 33MHz
             capabilities: pci pm pciexpress msi ht normal_decode bus_master cap_list
             configuration: driver=pcieport
             resources: irq:0 ioport:d000(size=4096) memory:fe900000-fe9fffff ioport:e0000000(size=270532608)
           *-display
                description: VGA compatible controller
                product: Baffin [Radeon RX 460/560D / Pro 450/455/460/555/555X/560/560X]
                vendor: Advanced Micro Devices, Inc. [AMD/ATI]
                physical id: 0
                bus info: pci@0000:28:00.0
                version: cf
                width: 64 bits
                clock: 33MHz
                capabilities: pm pciexpress msi vga_controller bus_master cap_list rom
                configuration: driver=amdgpu latency=0
                resources: irq:54 memory:e0000000-efffffff memory:f0000000-f01fffff ioport:d000(size=256) memory:fe900000-fe93ffff memory:c0000-dffff
           *-multimedia
                description: Audio device
                product: Advanced Micro Devices, Inc. [AMD/ATI]
                vendor: Advanced Micro Devices, Inc. [AMD/ATI]
                physical id: 0.1
                bus info: pci@0000:28:00.1
                version: 00
                width: 64 bits
                clock: 33MHz
                capabilities: pm pciexpress msi bus_master cap_list
                configuration: driver=snd_hda_intel latency=0
                resources: irq:51 memory:fe960000-fe963fff
        *-pci:2
             description: PCI bridge
             product: Family 17h (Models 00h-0fh) Internal PCIe GPP Bridge 0 to Bus B
             vendor: Advanced Micro Devices, Inc. [AMD]
             physical id: 7.1
             bus info: pci@0000:00:07.1
             version: 00
             width: 32 bits
             clock: 33MHz
             capabilities: pci pm pciexpress msi ht normal_decode bus_master cap_list
             configuration: driver=pcieport
             resources: irq:26 memory:fe200000-fe4fffff
           *-generic:0 UNCLAIMED
                description: Non-Essential Instrumentation
                product: Advanced Micro Devices, Inc. [AMD]
                vendor: Advanced Micro Devices, Inc. [AMD]
                physical id: 0
                bus info: pci@0000:29:00.0
                version: 00
                width: 32 bits
                clock: 33MHz
                capabilities: pm pciexpress cap_list
                configuration: latency=0
           *-generic:1 UNCLAIMED
                description: Encryption controller
                product: Family 17h (Models 00h-0fh) Platform Security Processor
                vendor: Advanced Micro Devices, Inc. [AMD]
                physical id: 0.2
                bus info: pci@0000:29:00.2
                version: 00
                width: 32 bits
                clock: 33MHz
                capabilities: pm pciexpress msi msix cap_list
                configuration: latency=0
                resources: memory:fe300000-fe3fffff memory:fe400000-fe401fff
           *-usb
                description: USB controller
                product: Family 17h (Models 00h-0fh) USB 3.0 Host Controller
                vendor: Advanced Micro Devices, Inc. [AMD]
                physical id: 0.3
                bus info: pci@0000:29:00.3
                version: 00
                width: 64 bits
                clock: 33MHz
                capabilities: pm pciexpress msi xhci bus_master cap_list
                configuration: driver=xhci_hcd latency=0
                resources: irq:48 memory:fe200000-fe2fffff
              *-usbhost:0
                   product: xHCI Host Controller
                   vendor: Linux 4.19.44-gentoo xhci-hcd
                   physical id: 0
                   bus info: usb@5
                   logical name: usb5
                   version: 4.19
                   capabilities: usb-2.00
                   configuration: driver=hub slots=4 speed=480Mbit/s
                 *-usb:0
                      description: Keyboard
                      product: Das Keyboard Model S
                      vendor: Metadot - Das Keyboard
                      physical id: 3
                      bus info: usb@5:3
                      version: 1.00
                      capabilities: usb-1.10
                      configuration: driver=usbhid maxpower=100mA speed=2Mbit/s
                 *-usb:1
                      description: USB hub
                      product: HighSpeed Hub
                      vendor: NEC Corp.
                      physical id: 4
                      bus info: usb@5:4
                      version: 1.00
                      capabilities: usb-2.00
                      configuration: driver=hub maxpower=100mA slots=2 speed=480Mbit/s
              *-usbhost:1
                   product: xHCI Host Controller
                   vendor: Linux 4.19.44-gentoo xhci-hcd
                   physical id: 1
                   bus info: usb@6
                   logical name: usb6
                   version: 4.19
                   capabilities: usb-3.00
                   configuration: driver=hub slots=4 speed=5000Mbit/s
        *-pci:3
             description: PCI bridge
             product: Family 17h (Models 00h-0fh) Internal PCIe GPP Bridge 0 to Bus B
             vendor: Advanced Micro Devices, Inc. [AMD]
             physical id: 8.1
             bus info: pci@0000:00:08.1
             version: 00
             width: 32 bits
             clock: 33MHz
             capabilities: pci pm pciexpress msi ht normal_decode bus_master cap_list
             configuration: driver=pcieport
             resources: irq:27 memory:fe800000-fe8fffff
           *-generic UNCLAIMED
                description: Non-Essential Instrumentation
                product: Advanced Micro Devices, Inc. [AMD]
                vendor: Advanced Micro Devices, Inc. [AMD]
                physical id: 0
                bus info: pci@0000:2a:00.0
                version: 00
                width: 32 bits
                clock: 33MHz
                capabilities: pm pciexpress cap_list
                configuration: latency=0
           *-storage
                description: SATA controller
                product: FCH SATA Controller [AHCI mode]
                vendor: Advanced Micro Devices, Inc. [AMD]
                physical id: 0.2
                bus info: pci@0000:2a:00.2
                version: 51
                width: 32 bits
                clock: 33MHz
                capabilities: storage pm pciexpress msi ahci_1.0 bus_master cap_list
                configuration: driver=ahci latency=0
                resources: irq:39 memory:fe808000-fe808fff
           *-multimedia
                description: Audio device
                product: Family 17h (Models 00h-0fh) HD Audio Controller
                vendor: Advanced Micro Devices, Inc. [AMD]
                physical id: 0.3
                bus info: pci@0000:2a:00.3
                version: 00
                width: 32 bits
                clock: 33MHz
                capabilities: pm pciexpress msi bus_master cap_list
                configuration: driver=snd_hda_intel latency=0
                resources: irq:52 memory:fe800000-fe807fff
        *-serial UNCLAIMED
             description: SMBus
             product: FCH SMBus Controller
             vendor: Advanced Micro Devices, Inc. [AMD]
             physical id: 14
             bus info: pci@0000:00:14.0
             version: 59
             width: 32 bits
             clock: 66MHz
             configuration: latency=0
        *-isa
             description: ISA bridge
             product: FCH LPC Bridge
             vendor: Advanced Micro Devices, Inc. [AMD]
             physical id: 14.3
             bus info: pci@0000:00:14.3
             version: 51
             width: 32 bits
             clock: 66MHz
             capabilities: isa bus_master
             configuration: latency=0
     *-pci:1
          description: Host bridge
          product: Family 17h (Models 00h-0fh) PCIe Dummy Host Bridge
          vendor: Advanced Micro Devices, Inc. [AMD]
          physical id: 101
          bus info: pci@0000:00:01.0
          version: 00
          width: 32 bits
          clock: 33MHz
     *-pci:2
          description: Host bridge
          product: Family 17h (Models 00h-0fh) PCIe Dummy Host Bridge
          vendor: Advanced Micro Devices, Inc. [AMD]
          physical id: 102
          bus info: pci@0000:00:02.0
          version: 00
          width: 32 bits
          clock: 33MHz
     *-pci:3
          description: Host bridge
          product: Family 17h (Models 00h-0fh) PCIe Dummy Host Bridge
          vendor: Advanced Micro Devices, Inc. [AMD]
          physical id: 103
          bus info: pci@0000:00:03.0
          version: 00
          width: 32 bits
          clock: 33MHz
     *-pci:4
          description: Host bridge
          product: Family 17h (Models 00h-0fh) PCIe Dummy Host Bridge
          vendor: Advanced Micro Devices, Inc. [AMD]
          physical id: 104
          bus info: pci@0000:00:04.0
          version: 00
          width: 32 bits
          clock: 33MHz
     *-pci:5
          description: Host bridge
          product: Family 17h (Models 00h-0fh) PCIe Dummy Host Bridge
          vendor: Advanced Micro Devices, Inc. [AMD]
          physical id: 105
          bus info: pci@0000:00:07.0
          version: 00
          width: 32 bits
          clock: 33MHz
     *-pci:6
          description: Host bridge
          product: Family 17h (Models 00h-0fh) PCIe Dummy Host Bridge
          vendor: Advanced Micro Devices, Inc. [AMD]
          physical id: 106
          bus info: pci@0000:00:08.0
          version: 00
          width: 32 bits
          clock: 33MHz
     *-pci:7
          description: Host bridge
          product: Family 17h (Models 00h-0fh) Data Fabric: Device 18h; Function 0
          vendor: Advanced Micro Devices, Inc. [AMD]
          physical id: 107
          bus info: pci@0000:00:18.0
          version: 00
          width: 32 bits
          clock: 33MHz
     *-pci:8
          description: Host bridge
          product: Family 17h (Models 00h-0fh) Data Fabric: Device 18h; Function 1
          vendor: Advanced Micro Devices, Inc. [AMD]
          physical id: 108
          bus info: pci@0000:00:18.1
          version: 00
          width: 32 bits
          clock: 33MHz
     *-pci:9
          description: Host bridge
          product: Family 17h (Models 00h-0fh) Data Fabric: Device 18h; Function 2
          vendor: Advanced Micro Devices, Inc. [AMD]
          physical id: 109
          bus info: pci@0000:00:18.2
          version: 00
          width: 32 bits
          clock: 33MHz
     *-pci:10
          description: Host bridge
          product: Family 17h (Models 00h-0fh) Data Fabric: Device 18h; Function 3
          vendor: Advanced Micro Devices, Inc. [AMD]
          physical id: 10a
          bus info: pci@0000:00:18.3
          version: 00
          width: 32 bits
          clock: 33MHz
          configuration: driver=k10temp
          resources: irq:0
     *-pci:11
          description: Host bridge
          product: Family 17h (Models 00h-0fh) Data Fabric: Device 18h; Function 4
          vendor: Advanced Micro Devices, Inc. [AMD]
          physical id: 10b
          bus info: pci@0000:00:18.4
          version: 00
          width: 32 bits
          clock: 33MHz
     *-pci:12
          description: Host bridge
          product: Family 17h (Models 00h-0fh) Data Fabric: Device 18h; Function 5
          vendor: Advanced Micro Devices, Inc. [AMD]
          physical id: 10c
          bus info: pci@0000:00:18.5
          version: 00
          width: 32 bits
          clock: 33MHz
     *-pci:13
          description: Host bridge
          product: Family 17h (Models 00h-0fh) Data Fabric: Device 18h; Function 6
          vendor: Advanced Micro Devices, Inc. [AMD]
          physical id: 10d
          bus info: pci@0000:00:18.6
          version: 00
          width: 32 bits
          clock: 33MHz
     *-pci:14
          description: Host bridge
          product: Family 17h (Models 00h-0fh) Data Fabric: Device 18h; Function 7
          vendor: Advanced Micro Devices, Inc. [AMD]
          physical id: 10e
          bus info: pci@0000:00:18.7
          version: 00
          width: 32 bits
          clock: 33MHz
     *-scsi:0
          physical id: 1
          logical name: scsi0
          capabilities: emulated
        *-disk
             description: ATA Disk
             product: KINGSTON SUV400S
             physical id: 0.0.0
             bus info: scsi@0:0.0.0
             logical name: /dev/sda
             version: 37R5
             serial: 50026B777601B343
             size: 223GiB (240GB)
             capabilities: gpt-1.00 partitioned partitioned:gpt
             configuration: ansiversion=5 guid=c8011386-7fb5-41e2-918c-f2d4437c9dcd logicalsectorsize=512 sectorsize=4096
           *-volume:0 UNCLAIMED
                description: Windows FAT volume
                vendor: mkfs.fat
                physical id: 1
                bus info: scsi@0:0.0.0,1
                version: FAT32
                serial: 643d-759a
                size: 498MiB
                capacity: 499MiB
                capabilities: boot fat initialized
                configuration: FATs=2 filesystem=fat name=EFI System
           *-volume:1
                description: EXT4 volume
                vendor: Linux
                physical id: 2
                bus info: scsi@0:0.0.0,2
                logical name: /dev/sda2
                version: 1.0
                serial: 9c49febc-1b7a-4d65-b635-e3d3d394f3f6
                size: 1GiB
                capabilities: journaled extended_attributes large_files huge_files dir_nlink 64bit extents ext4 ext2 initialized
                configuration: created=2018-12-26 14:36:23 filesystem=ext4 lastmountpoint=/boot modified=2018-12-28 21:16:24 mounted=2018-12-28 16:04:42 name=Linux filesystem state=clean
           *-volume:2
                description: EXT4 volume
                vendor: Linux
                physical id: 3
                bus info: scsi@0:0.0.0,3
                logical name: /dev/sda3
                logical name: /
                version: 1.0
                serial: c457528e-7010-4403-a4f2-cd8aec42b077
                size: 222GiB
                capacity: 222GiB
                capabilities: journaled extended_attributes large_files huge_files dir_nlink recover 64bit extents ext4 ext2 initialized
                configuration: created=2018-12-26 14:36:25 filesystem=ext4 lastmountpoint=/ modified=2018-12-26 22:59:37 mount.fstype=ext4 mount.options=rw,noatime mounted=2019-05-26 16:17:30 name=Linux filesystem state=mounted
     *-scsi:1
          physical id: 2
          logical name: scsi1
          capabilities: emulated
        *-disk
             description: ATA Disk
             product: WDC WD1003FZEX-0
             vendor: Western Digital
             physical id: 0.0.0
             bus info: scsi@1:0.0.0
             logical name: /dev/sdb
             version: 1A01
             serial: WD-WCC6Y1YV2YYN
             size: 931GiB (1TB)
             capabilities: gpt-1.00 partitioned partitioned:gpt
             configuration: ansiversion=5 guid=850aa1e7-d23e-4ab8-958d-d9e661ee6a1a logicalsectorsize=512 sectorsize=4096
           *-volume
                description: LVM Physical Volume
                vendor: Linux
                physical id: 1
                bus info: scsi@1:0.0.0,1
                logical name: /dev/sdb1
                serial: MOUvo4-62jP-2zkZ-SdGE-m2SD-t5UF-heBhY3
                size: 931GiB
                capabilities: multi lvm2
     *-scsi:2
          physical id: 3
          logical name: scsi6
          capabilities: emulated
        *-disk
             description: ATA Disk
             product: ST9250315AS
             vendor: Seagate
             physical id: 0.0.0
             bus info: scsi@6:0.0.0
             logical name: /dev/sde
             version: BSM1
             serial: 5VC18QWT
             size: 232GiB (250GB)
             capabilities: partitioned partitioned:dos
             configuration: ansiversion=5 logicalsectorsize=512 sectorsize=512 signature=f23a95d0
           *-volume
                description: Windows NTFS volume
                physical id: 1
                bus info: scsi@6:0.0.0,1
                logical name: /dev/sde1
                version: 3.1
                serial: 127d0ae2-5f1e-fb4e-8465-9bcf81b97884
                size: 232GiB
                capacity: 232GiB
                capabilities: primary ntfs initialized
                configuration: clustersize=4096 created=2015-11-21 11:06:04 filesystem=ntfs label=backup modified_by_chkdsk=true mounted_on_nt4=true resize_log_file=true state=dirty upgrade_on_mount=true
  *-network:0 DISABLED
       description: Ethernet interface
       physical id: 1
       logical name: virbr0-nic
       serial: 52:54:00:c4:a6:52
       size: 10Mbit/s
       capabilities: ethernet physical
       configuration: autonegotiation=off broadcast=yes driver=tun driverversion=1.6 duplex=full link=no multicast=yes port=twisted pair speed=10Mbit/s
  *-network:1
       description: Ethernet interface
       physical id: 2
       logical name: virbr0
       serial: 52:54:00:c4:a6:52
       capabilities: ethernet physical
       configuration: broadcast=yes driver=bridge driverversion=2.3 firmware=N/A ip=192.168.100.1 link=yes multicast=yes
  *-network:2
       description: Ethernet interface
       physical id: 3
       logical name: vnet0
       serial: fe:54:00:44:4a:b3
       size: 10Mbit/s
       capabilities: ethernet physical
       configuration: autonegotiation=off broadcast=yes driver=tun driverversion=1.6 duplex=full link=yes multicast=yes port=twisted pair speed=10Mbit/s
```
