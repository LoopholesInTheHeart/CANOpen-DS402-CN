
- [5. ����ԭ��](#5-����ԭ��)
    - [5.1. ����/����](#51-���Խ���)
    - [5.2. ͨ���������б�׼��](#52-ͨ���������б�׼��)
    - [5.3. �����ֵ�](#53-�����ֵ�)
        - [5.3.1. ��������������ʹ��](#531-��������������ʹ��)


---

## 5. ����ԭ��  
>OPERATING PRINCIPLE

### 	5.1. ����/���� 
>Introduction 

�������ļ���Ŀ����ΪCAN�����ϵ��������ṩ������Ҷ��ص���Ϊ�� �������������˶����Ƶ�CANopen�豸�����ļ������ڳ�ΪCANopen��CANͨ�������ļ�֮�ϣ�������CAN�����������豸ͨ�õĻ���ͨ�Ż��ơ�
>The purpose of this profile is, to give drives an understandable and unique behavior on the CANnetwork. The CANopen Device Profile for Drives and Motion Control is built on top of a CANcommunication profile, called CANopen, describing the basic communication mechanisms common toall devices at the CAN-network.

������Ԫ��Ŀ���ǽ���������������˶����Ʋ�Ʒ���ӵ�CAN���ߡ� ���ǿ��Խ���ͨ������I/O���õķ������ݶ���������������Ϣ��������չ������Ӧ�ó�����ض������� ������ʱ������ͨ����ѯ���¼��������жϣ�ͨ��CAN���ߴ�������Ԫ��ȡ���ݡ�
>The purpose of drive units is to connect axle controllers or other motion control products to the CAN bus. They can receive configuration information what is done via service data objects normally for I/O configurations, limit parameters for scaling or application specific parameters. At run time, data can be obtained from the drive unit via CAN bus by either polling or event driven (interrupt).

�˶����Ʋ�Ʒ��������ʵʱ�����Ĺ������ݶ���ӳ��(PDO)�������ʹ�÷������ݶ���(SDO)�����ã��μ�/3/���� ��ͨ���ŵ����ڽ���ʵʱ���ݣ����趨���ʵ��ֵ����λ��ʵ��ֵ
>The motion control products have a process data object mapping for real time operation, which may be configured using service data objects (see /3/). This communication channel is used to interchange real-time data like set-points or actual values like a position actual value e.g.

### 	5.2. ͨ���������б�׼�� 
>Standardization via profiling. 
	
�豸�淶�������ļ�������������Ҫ�ŵ�����ϵͳ���ɺ��豸��׼����
>The two principal advantages of the profile approach for device specification are in the areas of system integration and device standardization. 

������������豸��������Ʊ���ͨ�ŵĲ�Ʒ�������Ϊ�����������ṩ��һ�������̵��豸�淶����ʹ������Ʒ���ݣ��� ��Щ�淶����ʽ�����﷽�潫��˾���졣 �豸�����ļ��ĸ����ṩ�����ɴ���淶�ı�׼�� ͨ���������ַ��������������̶��������Ƶķ�ʽָ�����ǵ��豸�����������ϵͳ���ɵĹ�������
>If two independent device manufacturers design products that have to communicate, then both manufacturers must be provided with a device specification from the other one. These specifications will widely differ in formal and terminological aspects from one company to another. The concept of device profiling provides a standard for producing such specifications. By adopting this approach, all manufacturers will specify their devices in a similar fashion, what greatly reduces the effort involved in system integration.

�����豸�淶�������ļ��ķ�������һ���Ե��ŵ��ǣ�����������ָ��������������׼���豸�� ��׼���豸���ŵ�ܶࡣ ����Ҫ���ǣ���׼���豸��ϵͳ���������ض���Ӧ�̷��롣 ���һ����Ӧ���޷����������Ӧ������ϵͳ�����Ա�������ɵ�ʹ��������Ӧ���ṩ���豸�� ��һ���棬�豸�����̲��ٱ���Ϊÿ���ͻ�ʵʩ˽��Э�顣
>The other obvious advantage of the profile approach for device specification is, that it can be used to guide manufacturers into producing standardized devices. The advantages of standardized devices are numerous. Perhaps most important is the idea, that a standardized device decouples a system integrator from a specific supplier. If one supplier cannot meet special application demands, a system designer can use devices from another supplier with reduced effort. On the other hand the device manufacturers are not forced any more to implement private protocols for each customer.

�豸�����ļ������ˡ���׼���豸�� �˱�׼�豸���������Ļ������ܣ����豸���е�ÿ���豸������֧�֡� ����ǿ���Թ��ܶ���ȷ�����ټ򵥵ķ��������ض����豸�����Ǳ�Ҫ�ġ� ���磬��׼������Ԫ�ṩ������ֹͣ��������ֹͣ�������� �˹��ܱ�����Ϊ���蹦�ܣ���˿���ʹ����ͬ����Ϣ��֧ͣ�����������˶����Ƶ�CANopen�豸�����ļ����κ���������Ԫ��
>A device profile defines a ��standard�� device. This standard device represents really basic functionality, every device within this device class must support. This mandatory functionality is necessary to ensure, that at least simple non-manufacturer-specific operation of a device is possible. For example the standard drive unit provides a 'Quick stop' function to stop a drive. This function is defined as mandatory, such that any drive unit supporting the CANopen Device Profile for Drives and Motion Control, can be halted using the same message. 

�豸��׼���ĸ���ͨ����׼���豸�����ļ��ж���Ŀ�ѡ���ܵĸ��������չ�� ���������̶����ر���ʵ�����ֿ�ѡ���ܡ� ���ǣ����������ʵʩ���ֹ��ܣ��������Թ̶��ķ�ʽ��������
>The concept of device standardization is extended by the notion of optional functionality defined within the standardized device profile. Such optional functionality does not have to be implemented by all manufacturers. However, if a manufacturer implements such functionality he must do so in a fixed manner.

�ṩ��ѡ������һ�ַǳ�ǿ��Ļ��ƣ���ȷ�������������Զ���ķ�ʽʵ���ض����ܡ� ���磬�豸�����ļ�Ҳ��������ģ�飬����Ȼ���Ǻܳ����� ͨ������Բ�ͬ��ı�׼�����ʣ����Բ�ͬ�����̵Ľ����豸��ø����ס�
>Providing optional functionality is a very powerful mechanism to ensure all manufacturers implementing particular functionality in a defined fashion. For example, the device profile covers multiaxles modules as well, which are still not very common. By defining a standardized access to the different axles, interchanging devices from different manufacturers becomes easier. 

�豸�����ļ��ṩ��һ�ֻ��ƣ�ϣ��ʵ���������������ض����ܵ�������Ҳ������������ ����Ȼ�Ǳ�Ҫ�ģ���Ϊ�޷�Ԥ�����п��ܵ��豸���ܲ���ÿ���豸��Ŀ�ѡ����ж������� ��һ���֤�˱�׼�豸�����ļ�������δ������
>The device profiles provide a mechanism by which manufacturers wishing to implement truly manufacturer specific functionality can do so as well. This is clearly necessary since it would be impossible to anticipate all possible device functionality and define this in the optional category of each device class. This concept guarantees that the standard device profiles are 'future-proof'. 

ͨ������ǿ���豸���ԣ����Ա�֤��������������� ͨ�������ѡ���豸���ܣ���������һ���̶ȵ�����ԡ�ͨ��Ϊ�������ض��Ĺ������¡����ӡ��������̽����������ڹ�ʱ�ı�׼��
>By defining mandatory device characteristics, basic network operation is guaranteed. By defining optional device features a degree of defined flexibility can be built in. By leaving 'hooks' for manufacturer specific functionality, manufacturers will not be constrained to an out-of-date standard.


### 	5.3. �����ֵ� 
>The object dictionary 

�豸�����ļ�������Ҫ�Ĳ����Ƕ����ֵ������� �����ֵ䱾������ͨ�������������Ԥ���巽ʽ���ʵĶ���ķ��顣 ʹ��16λ�������ֵ��е�ÿ���������Ѱַ�������ֵ�������65536����Ŀ��
>The most important part of a device profile is the object dictionary description. The object dictionary is essentially a grouping of objects accessible via the network in an ordered pre-defined fashion. Each object within the dictionary is addressed using a 16-bit index so that the object dictionary may contain a maximum of 65536 entries.

����Ĳ����������ֳ�����ϵͳ���豸�����ļ��ǽ���һ�µģ����/3/��
>The layout closely conforms with device profiles for other field bus systems and is described in detail in /3/. 

����6000h��9fffh���ı�׼���豸�����ļ��������һ���豸��ͬ���������ݶ�����Щ�豸����ͨ�������ȡ��д�롣�����������ļ�ʹ�ô�6000h��9fffh����Ŀ�������������������������ܡ��������Χ�ڣ�������ʵ��8���ᡣ���⣬��������������������ϵĿ�ѡI/Oģ�顣��ЩI/Oģ��������DS 401����/4/����Ҫ�󣬲��ҿ��Դ�������ʵ�֡����ڱ�׼��������������6000h��67ffh֮���л�������060h��0fffh��A000h��ffff������������������ͨ�Ż������������ļ�����ʹ�á�
>The standardized device profile area at indices 6000h through 9FFFh contains all data objects common to a class of devices that can be read or written via the network. The drives profile uses entries from 6000h to 9FFFh to describe the drive parameters and the drive functionality. Within this range up to 8 axles can be realized. Additional it is possible to describe optional I/O modules combined with the drive. These I/O modules must conform to DS 401 (see /4/) and can be implemented instead of an axle. For standard drives only the range 6000h to 67FFh  is mandatory. There are also two reserved areas at indices 060h through 0FFFh and A000h through FFFFh for future use by the communication or drive profile. 
	
���ڶ����豸������Χ6000h��67FFh����λ���£�
>For multi axles devices the object range 6000h to 67FFh is shifted as follows:


6000h to 67FFh axle 0 

6800h to 6FFFh axle 1 

7000h to 77FFh axle 2 

7800h to 7FFFh axle 3 

8000h to 87FFh axle 4 

8800h to 8FFFh axle 5 

9000h to 97FFh axle 6 

9800h to 9FFFh axle 7



####		5.3.1. ��������������ʹ�� 
>Index and sub-index usage 



---

***Communication architecture***

![ͨѶ��ϵ�ṹ.png](./GraphicsAndTables/Figure_2.png)  

ͼ2.ͨѶ��ϵ�ṹ
>Figure 2: Communication architecture

---
