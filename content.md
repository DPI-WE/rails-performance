# N+1s, Caching and Performance 🏎️

Two of the most common and easy-to-fix performance issues in Rails applications are "N+1" database queries and slow rendering of ERB templates.

- Solve N+1s with .includes and the bullet gem: [How to use .includes? in Rails 7](https://levelup.gitconnected.com/how-to-use-includes-in-rails-7-643b5e1451c4)
- Solve slow rendering of ERB with [fragment/"Russian doll" caching](https://guides.rubyonrails.org/caching_with_rails.html)

N+1s are something that I try to resolve as soon as I have an action working the way I want it to, even while prototyping. Throw the [bullet gem](https://github.com/flyerhzm/bullet) into your project right from the start.

View caching is something that I only do as needed, because it can add significant complexity to make sure you're not showing any of your users stale information.  Even though Rails makes it as easy as possible for us, there's a reason for the old saying that ["There are 2 hard problems in computer science: cache invalidation, naming things, and off-by-1 errors."](https://martinfowler.com/bliki/TwoHardThings.html)

You may also want to add [MiniProfiler](https://github.com/MiniProfiler/rack-mini-profiler) to your development environment to display a speed badge for every HTML page.
