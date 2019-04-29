# FragmentPreference
fragmentPreference
![](https://github.com/Bearrrrrr/FragmentPreference/blob/master/img/QQ%E5%9B%BE%E7%89%8720190429211426.png)
![](https://github.com/Bearrrrrr/FragmentPreference/blob/master/img/QQ%E5%9B%BE%E7%89%8720190429211434.png)
![](https://github.com/Bearrrrrr/FragmentPreference/blob/master/img/QQ%E5%9B%BE%E7%89%8720190429211437.png)
![](https://github.com/Bearrrrrr/FragmentPreference/blob/master/img/QQ%E5%9B%BE%E7%89%8720190429211449.png)
![](https://github.com/Bearrrrrr/FragmentPreference/blob/master/img/QQ%E5%9B%BE%E7%89%8720190429211454.png)
xml
<?xml version="1.0" encoding="utf-8"?>
<PreferenceScreen
	xmlns:android="http://schemas.android.com/apk/res/android">
	<!--默认defaultValue=false-->
<PreferenceCategory android:title="In-line preferences">
	<CheckBoxPreference
		android:title="Checkbox preference"
		android:summary="This is a checkbox"
		android:key="check_key">
	</CheckBoxPreference>
</PreferenceCategory>
	<PreferenceCategory android:title="Launch preferences">
		<EditTextPreference
			android:title="Edit text preference"
			android:summary="An example that uses an edit text dialog"
			android:key="edit_key"
			android:dialogTitle="enter your favorite animal">
		</EditTextPreference>
		<ListPreference
			android:title="List preference"
			android:dialogTitle="Choose one"
			android:entries="@array/name_list"
			android:entryValues="@array/value_list"
			android:summary="An example that uses a list dialog"
			android:key="list_key">
		</ListPreference>
	</PreferenceCategory>
    <PreferenceCategory android:title="Launch preferences">
<!--子屏幕-->
		<!--android:persistent="false" 有啥用-->
    <PreferenceScreen
        android:title="Screen preference"
        android:summary="Shows another screen of preferences"
		>
		<CheckBoxPreference
			android:title="Toggle preference"
			android:summary="Preference that is on the next screen but same hierarchy"
			android:key="check_toggle_key"
			>
		</CheckBoxPreference>
    </PreferenceScreen>
        <Preference android:title="Intent preference"
            android:summary="Launches an Activity from an Intent">
            <intent android:action="android.intent.action.VIEW"
                android:data="http://www.baidu.com" />
        </Preference>
    </PreferenceCategory>
	<PreferenceCategory android:title="Preference attributes">
		<CheckBoxPreference
			android:title="Parent checkbox preference"
			android:summary="This is visually a parent "
			android:key="check_parent_key">
		</CheckBoxPreference>
		<CheckBoxPreference
			android:title="Child checkbox preference"
			android:summary="This is visually a child "
			android:key="check_child_key"
			android:dependency="check_parent_key">
		</CheckBoxPreference>
	</PreferenceCategory>
</PreferenceScreen>
