class Joe < Thor
  desc "download", "download the Selenium jar file from Google Code repository"
  def download
    url = "http://selenium-release.storage.googleapis.com/2.43/selenium-server-standalone-2.43.1.jar"
    file = File.join("tmp", File.basename(url))

    FileUtils.mkdir_p("tmp")

    system "wget #{url} -O #{file}" unless File.exist?(file)

    FileUtils.mv("#{file}", "vendor/selenium-server.jar")
  end
end
