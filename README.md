
# oss-common-dependencies
Common dependencies for home1-oss projects.

Java enterprise software relies on a lot of open source software.
There are lots of transitive dependency conflicts.

oss-common-dependencies is trying to build a stable dependency baseline for home1-oss modules.
If you are a user of home1-oss, you should use oss-release, not oss-common-dependencies.

Your project can use oss-release as parent and implicitly use oss-build as ancestor.

    <parent>
        <groupId>cn.home1</groupId>
        <artifactId>oss-release-spring-boot-${spring-boot.version}</artifactId>
        <version>${oss-release.version}</version>
    </parent>

or import in dependencyManagement.

    <!-- Use oss-build as parent is optional -->
    <parent>
        <groupId>cn.home1</groupId>
        <artifactId>oss-build</artifactId>
        <version>${oss-build.version}</version>
    </parent>
    <dependencyManagement>
        <dependencies>
            <dependency>
                <groupId>cn.home1</groupId>
                <artifactId>oss-release-spring-boot-${spring-boot.version}</artifactId>
                <version>${oss-release.version}</version>
                <type>pom</type>
                <scope>import</scope>
            </dependency>
        </dependencies>
    </dependencyManagement>
