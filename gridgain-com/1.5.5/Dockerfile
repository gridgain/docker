#
# Licensed to the Apache Software Foundation (ASF) under one or more
# contributor license agreements.  See the NOTICE file distributed with
# this work for additional information regarding copyright ownership.
# The ASF licenses this file to You under the Apache License, Version 2.0
# (the "License"); you may not use this file except in compliance with
# the License.  You may obtain a copy of the License at
#
#      http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#

# Start from a Java image.
FROM java:7

# Ignite version
ENV GRIDGAIN_VERSION 1.5.5

WORKDIR /opt/gridgain

ADD http://www.gridgain.com/media/gridgain-community-fabric-$GRIDGAIN_VERSION.zip /opt/gridgain/gridgain-community.zip

# Ignite home
ENV IGNITE_HOME /opt/gridgain/gridgain-community-fabric-$GRIDGAIN_VERSION

RUN unzip gridgain-community.zip

RUN rm gridgain-community.zip

# Copy sh files and set permission
ADD ./run.sh $IGNITE_HOME/

RUN chmod +x $IGNITE_HOME/run.sh

CMD $IGNITE_HOME/run.sh

EXPOSE 11211 47100 47500 49112