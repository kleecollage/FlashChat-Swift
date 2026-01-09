platform :ios, '15.0'

target 'Flash Chat iOS13' do
  use_frameworks! :linkage => :static
  
  pod 'CLTypingLabel'
  pod 'FirebaseAuth'
  pod 'FirebaseFirestore'

end

post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '15.0'
      config.build_settings['BUILD_LIBRARY_FOR_DISTRIBUTION'] = 'YES'
      config.build_settings['CLANG_WARN_QUOTED_INCLUDE_IN_FRAMEWORK_HEADER'] = 'NO'
      
      xcconfig_path = config.base_configuration_reference.real_path
      xcconfig = File.read(xcconfig_path)
      xcconfig_mod = xcconfig.gsub(/DT_TOOLCHAIN_DIR/, "TOOLCHAIN_DIR")
      
      File.open(xcconfig_path, "w") { |file| file << xcconfig_mod }
    end
  end
end
