# macvfx-recipes

Recipes for use with [AutoPkg](http://autopkg.github.io/autopkg/).
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
	<key>Comment</key>
	<string>Created with Recipe Robot v2.0.0 (https://github.com/homebysix/recipe-robot)</string>
	<key>Description</key>
	<string>Downloads the latest version of Postlab and imports it into Munki.</string>
	<key>Identifier</key>
	<string>com.macvfx.munki.Postlab</string>
	<key>Input</key>
	<dict>
		<key>MUNKI_REPO_SUBDIR</key>
		<string>apps/%NAME%</string>
		<key>NAME</key>
		<string>Postlab</string>
		<key>pkginfo</key>
		<dict>
			<key>catalogs</key>
			<array>
				<string>testing</string>
			</array>
			<key>description</key>
			<string>Collaborating with other editors was never this easy.</string>
			<key>developer</key>
			<string>The Sync Factory</string>
			<key>display_name</key>
			<string>Postlab</string>
			<key>name</key>
			<string>%NAME%</string>
			<key>unattended_install</key>
			<true/>
		</dict>
	</dict>
	<key>MinimumVersion</key>
	<string>1.0.0</string>
	<key>ParentRecipe</key>
	<string>com.macvfx.download.Postlab</string>
	<key>Process</key>
	<array>
		<dict>
			<key>Arguments</key>
			<dict>
				<key>pkg_path</key>
				<string>%pathname%</string>
				<key>repo_subdirectory</key>
				<string>%MUNKI_REPO_SUBDIR%</string>
			</dict>
			<key>Processor</key>
			<string>MunkiImporter</string>
		</dict>
	</array>
</dict>
</plist>
