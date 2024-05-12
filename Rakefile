# frozen_string_literal: true

require 'bundler/gem_tasks'
require 'rubocop/rake_task'
require 'rspec/core/rake_task'
require 'steep'
require 'steep/cli'

RuboCop::RakeTask.new
RSpec::Core::RakeTask.new(:spec)

desc "Type check with Steep"
task :steep do
  Steep::CLI.new(argv: ["check"], stdout: $stdout, stderr: $stderr, stdin: $stdin).run
end

task default: [:spec, :steep]
