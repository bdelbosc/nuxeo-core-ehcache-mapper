# Nuxeo Unified VCS Row Cache

This addon implements a VCS CachingMapper that use a unified ehcache.
This is an EXPERIMENTAL implementation, not for production use.

## Configuration

The name of the ehcache is "unifiedVCSCache".

To enable this addon you need to configure the repository by adding the 
following configuration in "default-repository-config.xml" inside the "repository"
tag:

    <cachingMapper enabled="true" class="org.nuxeo.ecm.core.storage.sql.UnifiedCachingMapper">
      <property name="ehcacheFilePath">/full/path/to/vcs-ehcache.xml</property>
    </cachingMapper>


There are 2 examples of ehcache configuration in the
src/main/resources/ directory, there is one that enable the ehcache XA
mode and should provide the same isolation as the default SoftRef
cache.

Please refer to [ehcache documentation] [5] for information about the ehcache configuration.

[5]: http://ehcache.org/apidocs/net/sf/ehcache/Cache.html#Cache%28java.lang.String,%20int,%20boolean,%20boolean,%20long,%20long%29

## About Nuxeo

Nuxeo provides a modular, extensible Java-based [open source software platform for enterprise content management] [1] and packaged applications for [document management] [2], [digital asset management] [3] and [case management] [4]. Designed by developers for developers, the Nuxeo platform offers a modern architecture, a powerful plug-in model and extensive packaging capabilities for building content applications.

[1]: http://www.nuxeo.com/en/products/ep
[2]: http://www.nuxeo.com/en/products/document-management
[3]: http://www.nuxeo.com/en/products/dam
[4]: http://www.nuxeo.com/en/products/case-management

More information on: <http://www.nuxeo.com/>



