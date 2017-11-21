---
layout: default
title:  "Setup Jekyll"
categories: main
---

1º	First, verify if our OS is 64 Bit
	WIN + Pause/Break

2º	Open PowerShell in Administrator Mode
	WIN, PowerShell [Right Click] Run as Administrator
	"Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux"

2ºb	Open Settings -> Update and Security -> For developers
	Turn on Developer Mode
	Open the Windows Store and install Ubuntu

3º Create user (location: %localappdata%\lxss\.)

# Install Jekyll and Bundler gems through RubyGems
gem install jekyll bundler

# Create a new Jekyll site at ./myblog
jekyll new myblog

# Change into your new directory
cd myblog

# Build the site on the preview server
bundle exec jekyll serve

# Now browse to http://localhost:4000

Ruby needed