forge 'https://forge.puppet.com'

# Profiles, even when they lived within a control repository were nothing more
# than a module with the arbitrary name of "profile". The important part of the
# concept is that there is a composition layer within your code base that
# unifies a highly differentiated set of module from disperate sources so they
# function for your organization, also providing a consistent data lookup
# strategy
#
# In larger organizations though, there is a massive number of stake holders and
# applications that could be affected by a single change in a shared layer that
# makes shipping an infrastructure-as-code release arduous. Instead define the
# standard for what a profile is inside the organizations and give each
# individual team responsible for a subset of the infrastructure their own
# profile module when they can compose with the highest level of context about
# what their applications need
#
# This example is illustrated best when CD4PE is leveraged to manage the
# shipping to "production" specific profile releases. This is because CD4PE can
# manage the version of each profile module validate it through impact analysis
# and conduct other tests before deployment
#
# https://puppet.com/docs/continuous-delivery/3.x/deploy_module.html
#
# Here we have two profile modules owned by internal teams and one owned by
# a group external to the organizations, e.g. managed service provider
# relationships
#
mod 'profile_enterprise_ops',
  :git            => 'https://github.com/ody/example-profile_enterprise_ops',
  :branch         => :control_branch,
  :default_branch => 'master'
mod 'profile_msp_ibm',
  :git            => 'https://github.com/ody/example-profile_msp_ibm',
  :branch         => :control_branch,
  :default_branch => 'master'
mod 'profile_cloud_ops',
  :git            => 'https://github.com/ody/example-profile_cloud_ops',
  :branch         => :control_branch,
  :default_branch => 'master'

# Core tech modules with explict versions set, which are the specific versions
# agreed upon by all automation stake holders of the organization and profiles
# are built upon. These can only be modified by cutting a new Puppet Environment
# for the purpose of development but must go through a full review with sign-off
# before being merged to a production release branch
mod 'puppetlabs/inifile',                    '4.1.0'
mod 'puppetlabs/stdlib',                     '6.2.0'
mod 'puppetlabs/firewall',                   '2.2.0'
mod 'puppetlabs-puppetserver_gem',           '1.1.1'
mod 'puppetlabs-bolt_shim',                  '0.3.0'
mod 'puppetlabs-ruby_task_helper',           '0.4.0'
mod 'fervid-secure_linux_cis',               '2.1.12'
mod 'trlinkin-noop',                         '1.0.1'
mod 'camptocamp-kmod',                       '2.5.0'
mod 'WhatsARanjit-node_manager',             '0.7.3'
mod 'puppetlabs-reboot',                     '3.0.0'
mod 'aboe/chrony',                           '0.3.2'
mod 'camptocamp/augeas',                     '1.9.0'
mod 'camptocamp/postfix',                    '1.10.0'
mod 'herculesteam/augeasproviders_core',     '2.6.0'
mod 'herculesteam/augeasproviders_grub',     '3.2.0'
mod 'herculesteam/augeasproviders_sysctl',   '2.5.0'
mod 'herculesteam/augeasproviders_shellvar', '4.0.0'
mod 'herculesteam/augeasproviders_pam',      '2.2.1'
mod 'kemra102/auditd',                       '2.2.0'
mod 'puppet/alternatives',                   '3.0.0'
mod 'puppet/cron',                           '2.0.0'
mod 'puppet/logrotate',                      '5.0.0'
mod 'puppetlabs/augeas_core',                '1.0.5'
mod 'puppetlabs/mailalias_core',             '1.0.6'
mod 'puppetlabs/mount_core',                 '1.0.4'
mod 'puppetlabs/ntp',                        '8.3.0'
mod 'puppet/cassandra',                      '3.0.0'
mod 'puppetlabs-docker',                     '3.10.0'
mod 'puppet-archive',                        '4.4.0'
mod 'puppetlabs-chocolatey',                 '5.0.2'
mod 'puppetlabs-java',                       '5.0.1'
