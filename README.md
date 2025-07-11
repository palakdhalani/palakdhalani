"use client"

import { Badge } from "@/components/ui/badge"
import { Button } from "@/components/ui/button"
import { Card, CardContent, CardDescription, CardHeader, CardTitle } from "@/components/ui/card"
import {
  Calendar,
  ExternalLink,
  GitFork,
  Github,
  Globe,
  Mail,
  MapPin,
  Star,
  Users,
  Code,
  BookOpen,
  Activity,
} from "lucide-react"

export default function Component() {
  const skills = [
    "JavaScript",
    "TypeScript",
    "React",
    "Next.js",
    "Node.js",
    "Express",
    "MongoDB",
    "PostgreSQL",
    "Python",
    "Django",
    "AWS",
    "Docker",
  ]

  const pinnedRepos = [
    {
      name: "e-commerce-platform",
      description: "Full-stack e-commerce platform built with Next.js, Node.js, and MongoDB",
      language: "TypeScript",
      stars: 124,
      forks: 32,
      topics: ["nextjs", "nodejs", "mongodb", "stripe"],
    },
    {
      name: "task-management-app",
      description: "Real-time task management application with drag-and-drop functionality",
      language: "JavaScript",
      stars: 89,
      forks: 21,
      topics: ["react", "express", "socket.io", "postgresql"],
    },
    {
      name: "weather-dashboard",
      description: "Beautiful weather dashboard with location-based forecasts and charts",
      language: "React",
      stars: 67,
      forks: 15,
      topics: ["react", "api", "charts", "responsive"],
    },
    {
      name: "blog-cms",
      description: "Content management system for blogs with markdown support",
      language: "Python",
      stars: 45,
      forks: 12,
      topics: ["django", "markdown", "cms", "blog"],
    },
  ]

  return (
    <div className="min-h-screen bg-gradient-to-br from-slate-50 to-slate-100 p-4">
      <div className="max-w-7xl mx-auto">
        {/* Header Section */}
        <div className="grid grid-cols-1 lg:grid-cols-3 gap-6 mb-8">
          {/* Profile Card */}
          <Card className="lg:col-span-1">
            <CardContent className="p-6">
              <div className="flex flex-col items-center text-center">
                <div className="w-32 h-32 rounded-full bg-gradient-to-r from-blue-500 to-purple-600 flex items-center justify-center text-white text-4xl font-bold mb-4">
                  PD
                </div>
                <h1 className="text-2xl font-bold mb-2">Palak Dhalani</h1>
                <p className="text-muted-foreground mb-4">Full Stack Web Developer</p>
                <p className="text-sm text-center mb-6">
                  Passionate about creating scalable web applications and beautiful user experiences. Always learning
                  new technologies and best practices.
                </p>

                <div className="flex flex-col gap-2 w-full text-sm">
                  <div className="flex items-center gap-2">
                    <MapPin className="w-4 h-4" />
                    <span>Mumbai, India</span>
                  </div>
                  <div className="flex items-center gap-2">
                    <Mail className="w-4 h-4" />
                    <span>palak.dhalani@email.com</span>
                  </div>
                  <div className="flex items-center gap-2">
                    <Globe className="w-4 h-4" />
                    <span>palakdhalani.dev</span>
                  </div>
                  <div className="flex items-center gap-2">
                    <Calendar className="w-4 h-4" />
                    <span>Joined GitHub in 2021</span>
                  </div>
                </div>

                <div className="flex gap-2 mt-6 w-full">
                  <Button className="flex-1" size="sm">
                    <Github className="w-4 h-4 mr-2" />
                    Follow
                  </Button>
                  <Button variant="outline" size="sm">
                    <Mail className="w-4 h-4" />
                  </Button>
                </div>
              </div>
            </CardContent>
          </Card>

          {/* Stats Cards */}
          <div className="lg:col-span-2 grid grid-cols-2 md:grid-cols-4 gap-4">
            <Card>
              <CardContent className="p-4 text-center">
                <div className="text-2xl font-bold text-blue-600">127</div>
                <div className="text-sm text-muted-foreground">Repositories</div>
              </CardContent>
            </Card>
            <Card>
              <CardContent className="p-4 text-center">
                <div className="text-2xl font-bold text-green-600">1.2k</div>
                <div className="text-sm text-muted-foreground">Followers</div>
              </CardContent>
            </Card>
            <Card>
              <CardContent className="p-4 text-center">
                <div className="text-2xl font-bold text-purple-600">892</div>
                <div className="text-sm text-muted-foreground">Following</div>
              </CardContent>
            </Card>
            <Card>
              <CardContent className="p-4 text-center">
                <div className="text-2xl font-bold text-orange-600">2.3k</div>
                <div className="text-sm text-muted-foreground">Stars</div>
              </CardContent>
            </Card>
          </div>
        </div>

        <div className="grid grid-cols-1 lg:grid-cols-3 gap-6">
          {/* Main Content */}
          <div className="lg:col-span-2 space-y-6">
            {/* Pinned Repositories */}
            <Card>
              <CardHeader>
                <CardTitle className="flex items-center gap-2">
                  <BookOpen className="w-5 h-5" />
                  Pinned Repositories
                </CardTitle>
              </CardHeader>
              <CardContent>
                <div className="grid grid-cols-1 md:grid-cols-2 gap-4">
                  {pinnedRepos.map((repo, index) => (
                    <Card key={index} className="border border-border hover:shadow-md transition-shadow">
                      <CardContent className="p-4">
                        <div className="flex items-start justify-between mb-2">
                          <h3 className="font-semibold text-blue-600 hover:underline cursor-pointer">{repo.name}</h3>
                          <ExternalLink className="w-4 h-4 text-muted-foreground" />
                        </div>
                        <p className="text-sm text-muted-foreground mb-3 line-clamp-2">{repo.description}</p>
                        <div className="flex flex-wrap gap-1 mb-3">
                          {repo.topics.map((topic, topicIndex) => (
                            <Badge key={topicIndex} variant="secondary" className="text-xs">
                              {topic}
                            </Badge>
                          ))}
                        </div>
                        <div className="flex items-center gap-4 text-sm text-muted-foreground">
                          <div className="flex items-center gap-1">
                            <div className="w-3 h-3 rounded-full bg-blue-500"></div>
                            {repo.language}
                          </div>
                          <div className="flex items-center gap-1">
                            <Star className="w-4 h-4" />
                            {repo.stars}
                          </div>
                          <div className="flex items-center gap-1">
                            <GitFork className="w-4 h-4" />
                            {repo.forks}
                          </div>
                        </div>
                      </CardContent>
                    </Card>
                  ))}
                </div>
              </CardContent>
            </Card>

            {/* Contribution Graph */}
            <Card>
              <CardHeader>
                <CardTitle className="flex items-center gap-2">
                  <Activity className="w-5 h-5" />
                  Contribution Activity
                </CardTitle>
                <CardDescription>2,847 contributions in the last year</CardDescription>
              </CardHeader>
              <CardContent>
                <div className="grid grid-cols-53 gap-1 mb-4">
                  {Array.from({ length: 371 }, (_, i) => (
                    <div
                      key={i}
                      className={`w-3 h-3 rounded-sm ${
                        Math.random() > 0.7
                          ? "bg-green-500"
                          : Math.random() > 0.5
                            ? "bg-green-300"
                            : Math.random() > 0.3
                              ? "bg-green-200"
                              : "bg-gray-200"
                      }`}
                    />
                  ))}
                </div>
                <div className="flex items-center justify-between text-sm text-muted-foreground">
                  <span>Less</span>
                  <div className="flex items-center gap-1">
                    <div className="w-3 h-3 rounded-sm bg-gray-200"></div>
                    <div className="w-3 h-3 rounded-sm bg-green-200"></div>
                    <div className="w-3 h-3 rounded-sm bg-green-300"></div>
                    <div className="w-3 h-3 rounded-sm bg-green-500"></div>
                  </div>
                  <span>More</span>
                </div>
              </CardContent>
            </Card>
          </div>

          {/* Sidebar */}
          <div className="space-y-6">
            {/* Skills */}
            <Card>
              <CardHeader>
                <CardTitle className="flex items-center gap-2">
                  <Code className="w-5 h-5" />
                  Skills & Technologies
                </CardTitle>
              </CardHeader>
              <CardContent>
                <div className="flex flex-wrap gap-2">
                  {skills.map((skill, index) => (
                    <Badge
                      key={index}
                      variant="outline"
                      className="hover:bg-primary hover:text-primary-foreground transition-colors"
                    >
                      {skill}
                    </Badge>
                  ))}
                </div>
              </CardContent>
            </Card>

            {/* Recent Activity */}
            <Card>
              <CardHeader>
                <CardTitle className="flex items-center gap-2">
                  <Activity className="w-5 h-5" />
                  Recent Activity
                </CardTitle>
              </CardHeader>
              <CardContent className="space-y-4">
                <div className="flex gap-3">
                  <div className="w-2 h-2 rounded-full bg-green-500 mt-2"></div>
                  <div className="flex-1">
                    <p className="text-sm">
                      Pushed to <span className="font-semibold">main</span> in{" "}
                      <span className="text-blue-600">e-commerce-platform</span>
                    </p>
                    <p className="text-xs text-muted-foreground">2 hours ago</p>
                  </div>
                </div>
                <div className="flex gap-3">
                  <div className="w-2 h-2 rounded-full bg-blue-500 mt-2"></div>
                  <div className="flex-1">
                    <p className="text-sm">
                      Created repository <span className="text-blue-600">react-components-library</span>
                    </p>
                    <p className="text-xs text-muted-foreground">1 day ago</p>
                  </div>
                </div>
                <div className="flex gap-3">
                  <div className="w-2 h-2 rounded-full bg-purple-500 mt-2"></div>
                  <div className="flex-1">
                    <p className="text-sm">
                      Starred <span className="text-blue-600">vercel/next.js</span>
                    </p>
                    <p className="text-xs text-muted-foreground">3 days ago</p>
                  </div>
                </div>
              </CardContent>
            </Card>

            {/* Organizations */}
            <Card>
              <CardHeader>
                <CardTitle className="flex items-center gap-2">
                  <Users className="w-5 h-5" />
                  Organizations
                </CardTitle>
              </CardHeader>
              <CardContent>
                <div className="flex gap-2">
                  <div className="w-8 h-8 rounded bg-gradient-to-r from-red-500 to-pink-500 flex items-center justify-center text-white text-sm font-bold">
                    TC
                  </div>
                  <div className="w-8 h-8 rounded bg-gradient-to-r from-green-500 to-blue-500 flex items-center justify-center text-white text-sm font-bold">
                    OS
                  </div>
                  <div className="w-8 h-8 rounded bg-gradient-to-r from-purple-500 to-indigo-500 flex items-center justify-center text-white text-sm font-bold">
                    WD
                  </div>
                </div>
              </CardContent>
            </Card>
          </div>
        </div>
      </div>
    </div>
  )
}
