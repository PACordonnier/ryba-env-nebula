
# Nebula

OpenNebula is an open-source management platform to build IaaS private, public and hybrid clouds.

    module.exports =
      use:
        db_admin: implicit: true, module: 'ryba/commons/db_admin'
        node: './lib/nebula/node'
      configure: './lib/nebula/front/configure'
      commands:
        'prepare': ->
          options = @config.nebula.front
          @call './lib/nebula/front/prepare'
        'install': ->
          options = @config.nebula.front
          @call './lib/nebula/front/install', options
        'start': './lib/nebula/front/start'
        'stop': './lib/nebula/front/stop'
