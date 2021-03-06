---
layout : "page-downloads"
title: Downloads
url: "/downloads/"
---
<header class="page-header">
  <img class="page-header-logo" src="{{< misc/rel "/images/logo-big-shadowed.png" >}}" alt="Xpiks">

  <div class="row">
    <div class="small-12">
      <!-- Mac -->
      <div data-os="mac" class="tab-download-content">
        <h2>Xpiks for macOS</h2>
        <p>Download the Xpiks package, unpack and drag'n'drop it to the Applications.</p>
        <a class="button" href="https://github.com/ribtoks/xpiks/releases/download/v1.5.4.2/Xpiks-v1.5.4.dmg">Download</a>
      </div>
      <!-- /Mac -->
      <!-- windows -->
      <div data-os="windows" class="tab-download-content">
        <h2>Xpiks for Windows</h2>
        <p>Download the Xpiks zip archive, unpack it where you want and it's ready to go.</p>
        <div class="row">
          <div class="small-12 medium-offset-1 medium-5 columns">
            <a class="button" href="https://github.com/ribtoks/xpiks/releases/download/v1.5.4.2/Xpiks-v1.5.4.zip">Download</a> <br/> <span>For Windows 64-bit</span>
          </div>
          <div class="small-12 medium-5 columns">
            <a class="button button-grey" href="https://github.com/ribtoks/xpiks/releases/download/v1.5.2/Xpiks-v1.5.2-x32.zip">Download</a> <br/> <span>For Windows 32-bit</span>
          </div>
          <div class="medium-1 columns"></div>
        </div>
      </div>
      <!-- /windows -->
      <!-- Linux -->
      <div data-os="linux" class="tab-download-content">
        <h2>Xpiks for Linux</h2>
        <p>This is a universal AppImage package. Download it, allow execution as a program  <br/> in Properties and run. Read more about <a href="http://appimage.org/">AppImage here.</a></p>
        <a class="button" href="https://github.com/ribtoks/xpiks/releases/download/v1.5.4.2/Xpiks-v1.5.4-x86_64.AppImage">Download</a>
      </div>
      <!-- /Linux -->

    </div>
  </div>
</header>

<section class="section-platforms section-default">
<div class="row">
  <div class="small-12">
    <h2><a href='{{< misc/rel "/blog/2014/building-xpiks-alone" >}}'>Other platforms</a></h2>
    <div class="tabs-os-buttons-wrapper">
    <!-- mac-button -->
    <div data-os="mac" class="tabs-os-button small-6 columns">
      <div class="download-button-wrap">
        <div class="icon"><img src='{{<  misc/rel "/images/os/macos.png" >}}' alt="macos"></div> for <strong>macOS</strong>
      </div>
    </div>
  <!-- /mac-button -->
  <!-- windows-button -->
  <div data-os="windows" class="tabs-os-button small-6 columns">
    <div class="download-button-wrap">
      <div class="icon"> <img src='{{< misc/rel "/images/os/windows.png" >}}' alt="windows"> </div> for <strong>Windows</strong>
    </div>
  </div>
  <!-- /windows-button -->
  <!-- linux-button -->
  <div data-os="linux" class="tabs-os-button small-6 columns">
    <div class="download-button-wrap">
      <div class="icon"> <img src='{{< misc/rel "/images/os/linux.png" >}}' alt="linux"> </div> for <strong>Linux</strong>
    </div>
  </div>
  <!-- /linux-button -->
  </div>
</div>
</div>
</section>

{{< donate >}}

