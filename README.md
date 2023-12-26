# Hilfe1
Bei dem Versuch einen laser cutter über USB an zu schließen stürtzte mein Imac ab. i Mac mitte 2010, Monteray mit Opencore Lagacy Patcher 
panic(cpu 3 caller 0xffffff801ef1665a): kfree: addr 0xffffffba7b14bd16, size 2 (offs:0) not found in any zone @kalloc.c:2303
Panicked task 0xffffffb414e4b670: 165 threads: pid 0: kernel_task
Backtrace (CPU 3), panicked thread: 0xffffffaa7c418000, Frame : Return Address
0xffffff8ca1c73620 : 0xffffff801e679a3d mach_kernel : _handle_debugger_trap + 0x41d
0xffffff8ca1c73670 : 0xffffff801e7dca26 mach_kernel : _kdp_i386_trap + 0x116
0xffffff8ca1c736b0 : 0xffffff801e7cbd93 mach_kernel : _kernel_trap + 0x4d3
0xffffff8ca1c73700 : 0xffffff801e619a90 mach_kernel : _return_from_trap + 0xe0
0xffffff8ca1c73720 : 0xffffff801e679e0d mach_kernel : _DebuggerTrapWithState + 0xad
0xffffff8ca1c73840 : 0xffffff801e6795c6 mach_kernel : _panic_trap_to_debugger + 0x2b6
0xffffff8ca1c738a0 : 0xffffff801ef149d3 mach_kernel : _panic + 0x84
0xffffff8ca1c73990 : 0xffffff801ef1665a mach_kernel : _panic_with_thread_context + 0x1bb2
0xffffff8ca1c739d0 : 0xffffff801e689cd5 mach_kernel : _kalloc_type_var_impl + 0x175
0xffffff8ca1c73a30 : 0xffffff801ee01afb mach_kernel : _IOFree + 0x1b
0xffffff8ca1c73a50 : 0xffffff7fb8f56a78 wch.usb.usb : __ZN7wch_usb16merWriteCompleteEPvS0_ij + 0x6e
0xffffff8ca1c73a90 : 0xffffff8021522fd3 com.apple.iokit.IOUSBFamily : __ZN14AppleUSBDevice30IOUSBHostDeviceRequestCompleteEPvS0_ij + 0x105
0xffffff8ca1c73ae0 : 0xffffff8021607d3a com.apple.iokit.IOUSBHostFamily : __ZN13IOUSBHostPipe33rawBufferControlRequestCompletionEPvS0_ij + 0x14
0xffffff8ca1c73b00 : 0xffffff8021615296 com.apple.iokit.IOUSBHostFamily : __ZN17AppleUSBIORequest8completeEv + 0x1048
0xffffff8ca1c73cd0 : 0xffffff801ffe2aef com.apple.driver.usb.AppleUSBCommon : __ZN24AppleUSBRequestCompleter20completeRequestQueueEP11queue_entry + 0x2d1
0xffffff8ca1c73ee0 : 0xffffff801ffe2801 com.apple.driver.usb.AppleUSBCommon : __ZN24AppleUSBRequestCompleter12checkForWorkEv + 0x1ed
0xffffff8ca1c73f20 : 0xffffff801ee4326e mach_kernel : __ZN10IOWorkLoop15runEventSourcesEv + 0x13e
0xffffff8ca1c73f60 : 0xffffff801ee42897 mach_kernel : __ZN10IOWorkLoop10threadMainEv + 0x37
0xffffff8ca1c73fa0 : 0xffffff801e61919e mach_kernel : _call_continuation + 0x2e
      Kernel Extensions in backtrace:
         com.apple.driver.usb.AppleUSBCommon(1.0)[3FED699A-A9EC-3D4C-83FB-B99AEAC6839C]@0xffffff801ffe0000->0xffffff801ffe3fff
         com.apple.iokit.IOUSBHostFamily(1.2)[0D850FBB-D7C5-3A4E-AA21-D0B0DCD1C1FE]@0xffffff80215a7000->0xffffff8021638fff
            dependency: com.apple.driver.AppleBusPowerController(1.0)[662EA4D6-6EB4-3294-BD26-7E38FBD6862E]@0xffffff801fad5000->0xffffff801fad8fff
            dependency: com.apple.driver.AppleSMC(3.1.9)[B18C1982-0F27-33AD-9B14-D293FCF548C5]@0xffffff801fe6c000->0xffffff801fe84fff
            dependency: com.apple.driver.usb.AppleUSBCommon(1.0)[3FED699A-A9EC-3D4C-83FB-B99AEAC6839C]@0xffffff801ffe0000->0xffffff801ffe3fff
            dependency: com.apple.driver.AppleUSBHostMergeProperties(1.2)[79643F3C-067B-3115-ABA4-88C59FF42A27]@0xffffff80216ac000->0xffffff80216acfff
            dependency: com.apple.iokit.IOACPIFamily(1.4)[2FC10A0F-6F6B-39C3-B5BF-86B01FAFEFDF]@0xffffff8020d79000->0xffffff8020d7afff
         com.apple.iokit.IOUSBFamily(900.4.2)[AC555F26-2FED-30DF-9ADD-9A6D05C893F3]@0xffffff80214fa000->0xffffff802155efff
            dependency: com.apple.driver.usb.AppleUSBCommon(1.0)[3FED699A-A9EC-3D4C-83FB-B99AEAC6839C]@0xffffff801ffe0000->0xffffff801ffe3fff
            dependency: com.apple.iokit.IOPCIFamily(2.9)[116B27E9-BAAB-34E5-87E5-E7D14B436CBF]@0xffffff8021222000->0xffffff802124efff
            dependency: com.apple.iokit.IOUSBHostFamily(1.2)[0D850FBB-D7C5-3A4E-AA21-D0B0DCD1C1FE]@0xffffff80215a7000->0xffffff8021638fff
         wch.usb.usb(1.0)[3273DEA2-F5D4-38B3-9CF8-5F1D9C4DBF75]@0xffffff7fb8f54000->0xffffff7fb8f5afff
            dependency: com.apple.iokit.IOSerialFamily(11)[59508FB1-359C-32AE-85AC-E212E5D6FF98]@0xffffff80212f0000->0xffffff80212f6fff
            dependency: com.apple.iokit.IOUSBFamily(900.4.2)[AC555F26-2FED-30DF-9ADD-9A6D05C893F3]@0xffffff80214fa000->0xffffff802155efff

Process name corresponding to current thread (0xffffffaa7c418000): kernel_task
Boot args: keepsyms=1 debug=0x100 -lilubetaall -btlfxallowanyaddr ipc_control_port_options=0 -nokcmismatchpanic -disable_sidecar_mac

Mac OS version:
21G1974

Kernel version:
Darwin Kernel Version 21.6.0: Thu Nov  9 00:38:19 PST 2023; root:xnu-8020.240.18.705.10~1/RELEASE_X86_64
Kernel UUID: ABAADB03-E25C-33B4-B3E0-574627B92635
KernelCache slide: 0x000000001e400000
KernelCache base:  0xffffff801e600000
Kernel slide:      0x000000001e410000
Kernel text base:  0xffffff801e610000
__HIB  text base: 0xffffff801e500000
System model name: iMac11,3 (Mac-F2238BAE)
System shutdown begun: NO
Panic diags file available: YES (0x0)
Hibernation exit count: 0

System uptime in nanoseconds: 14593860952
Last Sleep:           absolute           base_tsc          base_nano
  Uptime  : 0x0000000365dcadff
  Sleep   : 0x0000000000000000 0x0000000000000000 0x0000000000000000
  Wake    : 0x0000000000000000 0x0000000ac152da0f 0x0000000000000000
Compressor Info: 0% of compressed pages limit (OK) and 0% of segments limit (OK) with 0 swapfiles and OK swap space
Zone info:
  Zone map: 0xffffff9a7b0c0000 - 0xffffffba7b0c0000
  . PGZ   : 0xffffff9a7b0c0000 - 0xffffff9a7c8c1000
  . VM    : 0xffffff9a7c8c1000 - 0xffffff9f491f4000
  . RO    : 0xffffff9f491f4000 - 0xffffffa0e2a5a000
  . GEN0  : 0xffffffa0e2a5a000 - 0xffffffa5af38d000
  . GEN1  : 0xffffffa5af38d000 - 0xffffffaa7bcc0000
  . GEN2  : 0xffffffaa7bcc0000 - 0xffffffaf485f3000
  . GEN3  : 0xffffffaf485f3000 - 0xffffffb414f26000
  . DATA  : 0xffffffb414f26000 - 0xffffffba7b0c0000
  Metadata: 0xffffffffbb7ee000 - 0xffffffffdb7ee000
  Bitmaps : 0xffffffffdb7ee000 - 0xffffffffdffee000



