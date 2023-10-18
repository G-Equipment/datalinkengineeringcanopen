# datalinkengineeringcanopen
CANopen SDK (API) for Windows developers. Supported adapters: Kvaser, Ixxat, CANUSB, CAN232, Peak PCAN, Copley Controls, USBTIN and more.
See Youtube turtorial for more information:

https://www.youtube.com/channel/UC4UU3Yp9T2r1AMsZJywqCdQ

Forked by G-Equipment

# Modification
* \datalinkengineeringcanopen\canopen_stack_visual_studio_2022\visual_studio\plug_in_peak\canopenlib_hw_peak.cpp
    * Adding this to use PCIE Can Card
        ```C++
        #define USE_PCAN_PCI TRUE 
        ```
    * Adding this for being able to use 800k baudrate
        ```C++
        case 800000:
            can_port_data_devices[handle].bitrate = PCAN_BAUD_800K;
            canopen_res = CANOPEN_OK;
            break;
        ```        
* Modification in the CANopen_CPP_and_NET _only_64_bit_special_case_applications.sln for Release x64 CANOpen configuration

Branch master