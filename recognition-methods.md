# Recognition Methods {#recognition-methods}

The web platform offers many ways for a website to recognize that a [=person=]
is using the same [=identity=] over time, including [[RFC6265|cookies]],
{{WindowLocalStorage/localStorage}}, {{WindowOrWorkerGlobalScope/indexedDB}},
{{CacheStorage}}, and other forms of storage.

Sometimes sites use this to save the [=person=]'s preferences or ongoing activities
(e.g. shopping carts), and people have come to expect this behavior in some
[=contexts=].

People are unlikely to expect [=recognition=] all the time, and can find it
difficult to prevent or mitigate, especially if it is automated.

[=Recognition=] can be automated in different ways:

* through the use of <a data-cite="Browser-Parties#environment-cross-site">cross-site</a> cookies,
* by having someone navigate to a link that has been decorated with an identifier
  ([[?Nav-Tracking]]),
* collecting the same piece of identifying information on both sites, or
* by correlating the timestamps of an event that occurs nearly-simultaneously
on both sites (this is an example of a <a
href="https://github.com/asankah/ephemeral-fingerprinting/blob/2395a35aac260d4d2f880eeb05c2617b0fd642ea/README.md">timing
attack</a>).

Recognition can also be made *persistent* such that it will
defeat potential mitigations like [=partitions=] or clearing one's cookies.
This is unsanctioned tracking ([[?UNSANCTIONED-TRACKING]]) and can
take multiple forms:

* [=Fingerprinting=].
* [=Header enrichment=].
* [=Cross-device communication=].

<dfn data-lt="fingerprint">Fingerprinting</dfn> consists of using attributes of the [=person=]'s
browser and platform that are consistent between two or more visits and
probably unique to the person.

The attributes can be exposed as information about the [=person=]'s device
that on their own are benign (as opposed to [[[#hl-sensitive-information]]]).
Taken in the aggregate these attributes could uniquely identify the device, or
contribute to possible [=cross-context recognition=].
For example:

* language and time zone;
* window size;
* system preferences (such as dark mode, serif font, etc.).

Preventing [=fingerprinting=] can be particularly challenging in cases that
only affect a small group of people who use the web. For example, people who
configure their systems in unique ways, such as by using a browser with a very
small number of users.
See [[fingerprinting-guidance]] for how to mitigate threats that result from
[=fingerprinting=].

Supercookies occur when a user agent stores data for a site but makes that data more
difficult to clear than other cookies or storage, typically because of a bug, of features
relating to cache storage and network state (e.g. ETag, HSTS), or
because the browser restores the browser vendor's cookies when local state is cleared.
<a data-cite="fingerprinting-guidance#clearing-all-local-state">Fingerprinting
Guidance § Clearing all local state</a> discusses how specifications can help
user agents avoid this mistake.

<dfn>Header enrichment</dfn> happens when a network operator adds HTTP request headers
to identify their customers to sites that they visit. It is
difficult for a [=user agent=] to mitigate against [=header enrichment=].

<dfn>Cross-device communication</dfn> is communication
between code on one device and code running on another device. For example, sounds or
light emitted from one device could be detected by a microphone or light sensor on
another device [[?SILVERPUSH]]. [=Cross-device communication=] enables cross-device
tracking, a form of [=cross-context recognition=], and it can also be used for other
[=inappropriate=] information flows.
