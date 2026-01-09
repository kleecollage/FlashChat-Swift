# Uncomment the next line to define a global platform for your project
platform :ios, '15.0'

target 'Flash Chat iOS13' do
  # Comment the next line if you don't want to use dynamic frameworks
  pod 'CLTypingLabel'

  # Pods for Flash Chat iOS13
  pod 'CLTypingLabel'

end

post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['ALWAYS_EMBED_SWIFT_STANDARD_LIBRARIES'] = 'NO'
    end
  end
end
