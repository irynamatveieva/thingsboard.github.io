---
layout: docwithnav
assignees:
- nick
title: MQTT Sparkplug API
description: Supported MQTT Sparkplug API Reference for IoT Devices 

sparkplug-create-device-profile:
    0:
        image: /images/reference/sparkplug/sparkplug-create-device-profile-1-ce.png
        title: 'Navigate to the Device profiles page and click on the "+" icon in the device profile table header to open the Add device profile dialog. Use MQTT EoN Node as profile name or any other meaningful value;'
    1:
        image: /images/reference/sparkplug/sparkplug-create-device-profile-2-ce.png
        title: 'Navigate to Transport configuration tab and select the MQTT transport type. Make sure you have selected the “MQTT Sparkplug B Edge of Network (EoN) node” checkbox. Input the names of Sparkplug metrics you would like to store as attributes instead of time series data. This list should also include metrics you may want to update from the server side and push to the device;'
    2:
        image: /images/reference/sparkplug/sparkplug-create-device-profile-3-ce.png
        title: 'MQTT EoN Node have been created.'

sparkplug-create-device:
    0:
        image: /images/reference/sparkplug/sparkplug-create-device-1-ce.png
        title: 'Navigate to the Devices page and click on the “+” icon in the device table header to open the Add new device dialog. Input your EoN node device name (e.g. Node 1) and select the existing device profile: MQTT EoN Node. Click Add;'
    1:
        image: /images/reference/sparkplug/sparkplug-create-device-3-ce.png
        title: 'Navigate to the manage credentials and copy the access token. We will use it in the next step. Note that you may use other types of credentials as well.'

sparkplug-create-device-telemetry-and-attributes:
    0:
        image: /images/reference/sparkplug/sparkplug-device-latest-telemetry-1-ce.png
        title: 'Navigate to the details of the EoN node device and open the Latest telemetry tab. You should see the device metrics, for example Current Grid Voltage;'
    1:
        image: /images/reference/sparkplug/sparkplug-device-shared-attribute-1-ce.png
        title: 'Navigate to the Attributes tab and select Shared attributes scope. You should see metrics that you have previously configured in the Step 1.'

sparkplug-create-two-devices:
    0:
        image: /images/reference/sparkplug/sparkplug-created-two-devices-1-ce.png
        title: 'Navigate to the Devices table and note that two new Sparkplug devices are created by the emulator: "Sparkplug Device 1" and "Sparkplug Device 2";'
    1:
        image: /images/reference/sparkplug/sparkplug-created-two-devices-2-ce.png
        title: 'Both devices have their own attributes and telemetry values that are generated by the emulator.'

sparkplug-update-metrics-using-shared-attributes-1:
    0:
        image: /images/reference/sparkplug/sparkplug-edit-device-profile-1-ce.png
        title: 'Go to the Profiles -> Device profiles and select MQTT EoN Node device profile. In the Transport сonfiguration tab, add a new Sparkplug metric name — “Outputs/*".'

sparkplug-update-metrics-using-shared-attributes-2:
    0:
        image: /images/reference/sparkplug/sparkplug-new-attributes-1-ce.png
        title: 'Go back to the Devices page and select the Sparkplug Device 1. On the Shared attributes tab, you will see two new attributes: “Outputs/LEDs/Green” with the value “true” and “Outputs/LEDs/Yellow” with the value “false”. These are metrics that are saved as attributes, and we can modify them and send values to the device.'

sparkplug-update-metrics-using-shared-attributes-3:
    0:
        image: /images/reference/sparkplug/sparkplug-edit-attribute-1-ce.png
        title: 'Click on the “pencil” icon and change the value of the attribute “Outputs/LEDs/Green” from “true” to “false” by unchecking the corresponding box. Then, click Update.'

sparkplug-update-metrics-using-shared-attributes-4:
    0:
        image: /images/reference/sparkplug/sparkplug-edit-attribute-2-ce.png
        title: 'Now let’s change the value of the “Device Control/Scan Rate” attribute. Click on the “pencil” icon and change the value from “60000” to “30000”. Click Update.'

sparkplug-update-metrics-using-shared-attributes-5:
    0:
        image: /images/reference/sparkplug/sparkplug-edit-attribute-3-ce.png
        title: 'The new attribute values for "Outputs/LEDs/Green" and "Device Control/Scan Rate" have been successfully sent to the device.'

sparkplug-update-metrics-using-the-thingsboard-rpc-command-1:
    0:
        image: /images/reference/sparkplug/sparkplug-create-new-dashboard-1-ce.png
        title: 'Go to the Dashboard page and create a new dashboard named Sparkplug;'
    1:
        image: /images/reference/sparkplug/sparkplug-create-new-dashboard-2-ce.png
        title: 'Open the dashboard and add an alias by clicking on Entity Aliases icon on the top-right. Name the alias (EoN Node, for example), select filter type “Single Entity”, type “Device” and choose our Node 1. Press Add and then Save.'

sparkplug-update-metrics-using-the-thingsboard-rpc-command-2:
    0:
        image: /images/reference/sparkplug/sparkplug-create-new-dashboard-3-ce.png
        title: 'Click "Add New Widget";'
    1:
        image: /images/reference/sparkplug/sparkplug-create-new-dashboard-4-ce.png
        title: 'Select "Control widgets" from drop down menu;'
    2:
        image: /images/reference/sparkplug/sparkplug-create-new-dashboard-5-ce.png
        title: 'Select "RPC Button" widget;'
    3:
        image: /images/reference/sparkplug/sparkplug-create-new-dashboard-6-ce.png
        title: 'On the Data field select created alias;'
    4:
        image: /images/reference/sparkplug/sparkplug-create-new-dashboard-7-ce.png
        title: 'Go to "Advanced" tab and enter button label. In the RPC settings enter "RPC method" (command to the EoN Node) and "RPC method params". Click Add;'
    5:
        image: /images/reference/sparkplug/sparkplug-create-new-dashboard-8-ce.png
        title: 'Save changes.'

sparkplug-update-metrics-using-the-thingsboard-rpc-command-3:
    0:
        image: /images/reference/sparkplug/sparkplug-create-new-dashboard-9-ce.png
        title: 'Click "REBOOT NODE" button on the widget. In the Terminal, you will see a message indicating that the RPC command has been sent to the device and the Sparkplug EoN Node 1 has been rebooted.'

---

{% include get-hosts-name.html %}
{% include docs/reference/mqtt-sparkplug-api.md %}
