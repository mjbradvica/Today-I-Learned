# 1/1

When using NServiceBus with AzureServiceBus you need to have a topic and subscription
created in azure. NServiceBus configuration has to reference what topic to use.

# 1/2

gRPC has middleware that allow you to choose between a gRPC client and requests from gRPC web.
gRPC web is used by browsers because browsers can't support gRPC natively. Seems easier to use
the gRPC client though. gRPC Web is really just for browsers.